## January 16, 2021

I'm back on the wagon after binge watching [Date A Live](https://myanimelist.net/anime/15583/Date_A_Live) (don't judge lmao). It is good to take a mental break from learning and coding once in a while 😁

I decided to take a bit of a break from Angular and Japanese, and work on learning Swift.

## Swift

I came up an idea for a super basic app, essentially a clone of this website: https://nyanpass.com/. To summarize what the website does, it has a button that says "にゃぱすー" literally "Nyanpasu" and every time it is clicked it plays a sound file and increments a global counter. The sound is Renge from [Non Non Biyori](https://myanimelist.net/anime/17549/Non_Non_Biyori) (really wholesome anime) saying "Nyanpasu!". I decided to make a clone of this app so I can learn the basics of SwiftUI and making a very basic app.

The git repo is here: https://github.com/YoCodingJosh/Nyanpasu-iOS

The components that need to be implemented:

* A button that plays the sound
* A counter that counts how many times the sound is played locally (globally is wayyy outside the scope right now lol)

Today I worked on the first component, the button that plays sound. Which was a bit more complicated than it seems...

The button was super easy to add in SwiftUI.

```
var body: some View {
    Button(action: nyanpasu, label: {
        Text("Nyanpasu!")
    })
}
```

Now, playing the sound... that's where the biggest pain was.

I kept getting this error: `unexpectedly found nil while unwrapping an Optional value` while using the AVAudioPlayer object. I search on Google and none StackOverflow's links couldn't help me!

I solved it though! I MUST BE SOME 500 IQ, 4-D EYESIGHT, MASTERMIND HERE! Not really, it was my mistake to begin with.

You see, SwiftUI is a bit different than the ol' Interface Builder. SwiftUI's component graph is computed meaning that blah blah blah (I'm still new to SwiftUI btw). TL;DR: Trying to run code that can modify an instance variable (in my case the AVAudioPlayer instance) in the View struct is a no-no. That's what was confusing me. Once I extracted the logic into a separate file and setting the AVAudioPlayer instance a global, everything worked.

I did also think about how I'm going to store the number of times the button was pressed. I'm thinking about using Core Data. I could use something like `NSUbiquitousKeyValueStore` but that syncs with iCloud and dealing with that is a PITA when I want to keep things simple.

I think I'll work on that part later on (along with making the app look nice). Back to Angular and Japanese tomorrow! またね！
