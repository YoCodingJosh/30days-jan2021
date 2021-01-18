# January 17, 2021

## Angular

I ported the functionality that redirects the user to the MyAnimeList authorization page from the Express monolith to Angular. It wasn't hard to implement. Only weird thing was MAL was having some server problems (giving HTTP 500) while I was testing, which made me question my sanity for a hot minute. 😂

I also stubbed out the error page component and route for when authorization fails (either server error or user cancellation).

I'll have to start refactoring the Express API so it won't try to serve the error page and clean up the code in general (ie: remove all of the logic related to the frontend).

## Japanese

I did some Duolingo lessons, but I forgot what they were. ごめんね！ 
