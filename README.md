# Homework 7

ID_search is the function for MinMax algorithm.

MinMaxと言う関数がありますが使っていません。
メインの評価関数はSearchBestmoveです。

EvaluateBoardの評価は以下のように盤面上の石の位置に依存します。

|5000|-500|20|20|20|20|-500|5000|
|---|---|---|---|---|---|---|---|
|-500|-500|1|1|1|1|-500|-500|
|20|3|3|3|3|3|3|20|
|20|3|3|3|3|3|3|20|
|20|3|3|3|3|3|3|20|
|20|3|3|3|3|3|3|20|
|-500|-500|1|1|1|1|-500|-500|
|5000|-500|20|20|20|20|-500|5000|







--------------------------------------------------------------------------------
1. Fork a copy for your changes
2. Clone it to your local workstation
3. Create a new project to host your AI in https://console.cloud.google.com
4. Run `gcloud init` and select that new project.
5. `gcloud app deploy python/` or `gcloud app deploy go/` to deploy your app.
6. Add the appspot address to the ["Reversi Players" sheet](https://docs.google.com/spreadsheets/d/1UaFboojs_saqX-B4f1rAXhun74eTMdAQToo6_mGKQPs/edit)
7. **Modify the way a move is picked**
8. re-deploy the app
9. repeat steps 7 and 8 until you have a very clever AI :)
10. eventually push your awesome clever AI to github.
    * If you want to keep it secret until Thursday night, that's fine.
11. email step17 with your github repository link.

# Using reflector.go

You can use this "reflector" program to make a locally running dev_appserver instance act like a human player (i.e. you don't have to deploy the whole app to have it run a game).

To run it:
* [download](https://golang.org/dl/) and install Go if you don't have it already.
* Start a new game on https://step-reversi.appspot.com with a "Human (or Local bot)" selected as one of the players
* copy the URL of that browser tab showing that game (i.e. a URL that looks like "https://step-reversi.appspot.com/view?gamekey=fOoBaR")
* type `go run reflector.go "https://step-reversi.appspot.com/view?gamekey=fOoBaR"`
    * (but pasting your actual viewer URL there -- fOoBaR is not a real game ;)
