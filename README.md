# DDR Tools

This is web-app that allows random draw of songs from Dance Dance Revolution and other music games
with a variety of options for filtering which songs and charts are included. The intended use case
is in competitive tournaments or personal training.

The app is officially available at [https://ddr.tools/](https://ddr.tools/)
or as a downloadable zip file from the [releases page](https://github.com/noahm/DDRCardDraw/releases).
The app supports running fully offline, and can load and operate without an internet connection after
being loaded once in any modern web browser.

Original app by Jeff Lloyd; ongoing maintenance provided by [noahm](https://github.com/noahm)
and [FuriousDCSL](https://github.com/FuriousDCSL). Contributions are welcome!

## Customizing / Contributing

This app can be easily customized for any format a tournament might use, including adding song
data for other games. If you have requests or ideas, you're welcome reach out on [Facebook](https://m.me/noah.manneschmidt),
[Twitter](https://twitter.com/Cathadan), Discord (Cathadan#2431), or wherever else you can find me.

If you want to take a stab at it yourself, you will want to have node.js >= 14.0.0 installed along with
[yarn](https://yarnpkg.com/) and some familarity with React app development.

Clone this repo to your computer. Then the following commands will be useful:

```sh
# Before running anything else, do this!
# It's a one-time local install of dependencies needed to build the app.
yarn install

# local development will start, with app running at http://localhost:8080/
# edits to the files in ./src/ will automatically reload the browser
yarn start

# if you make changes to any game/song data in ./src/songs/ this will give
# a basic sanity check on the format and contents of it
yarn validate:json

# build a zipped, standalone copy of the app that runs entirely offline,
# jacket images and all! simply unzip somewhere and open index.html
yarn build:zip
```

There are some other useful scripts in `scripts/` that help in maintaining data integrity and pulling
in new song data. Several have top-level aliases so you can conveniently update song data:

```sh
# download latest StepManiaX song data and jackets
yarn import:smx

# download latest DDR A20 Plus song data and jackets (when available on RemyWiki)
yarn import:ddr
```

Ideas for future develoment are now being tracked as issues on this repo. Feel free to jump in if you
want to help build out something new!
