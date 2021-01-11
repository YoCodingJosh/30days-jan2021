# January 10, 2021

[It was a good day today.](https://i.imgur.com/FamPgLs.png) I watched a ton of anime. I completed two series [Is The Order a Rabbit?](https://myanimelist.net/anime/21273/Gochuumon_wa_Usagi_Desu_ka) and [Sakura Trick](https://myanimelist.net/anime/20047/Sakura_Trick) (don't judge lmao) and started the new season of [Non Non Biyori](https://myanimelist.net/anime/39808/Non_Non_Biyori_Nonstop).

## Japanese

I also practiced some Japanese. I reviewed some Hiragana (specifically Hiragana 4 on Duolingo) which went over some pronunciation and some words like まんが (manga), きっぷ (kippu = ticket), and くだもの (kudamono = fruit).

## Angular

I haven't been neglecting my Angular learning! I have been thinking (my brain hurts now) between anime episodes about the best tactic to refactor my code to allow for an Angular SPA frontend and an Express backend.

I'm going to do the work in the [`angular-rework` branch](https://github.com/YoCodingJosh/anime_stats/tree/angular-rework).

My biggest hangup about the Angular port are:

* Being able to deploy one code bundle and repo rather than having to maintain two separate code deployments and repositories for the UI and API.

I believe that this: https://angular.io/guide/universal may be useful to solve that hangup.

Either that or just do it the hard way and serve up the compiled Angular bundle on the application `/main` endpoint and set up Angular's webpack-dev-server to proxy the API calls to the API "server" running on a different port and at `/api`.
