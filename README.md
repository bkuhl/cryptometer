# Cryptometer

A Rainmeter extension for monitoring Cryptocurrencies.

![Widget Preview](https://image.ibb.co/fU43NQ/cryptometer_preview.png)

 > A [pull request is open](https://github.com/tjmarkham/win10widgets/pull/80) to merge this module into the skin itself.

### Features:

 * Tracks the top 5 Cryptocurrencies out of the box
 * Customizable with whatever currencies you'd like to track (see Managing Cryptocurrencies below)
 * Updates data every 15 minutes
 * Click the symbol to view graphs, charts and more

# Requirements
 * [Rainmeter 4.1+](https://www.rainmeter.net)
 * [Win10Widgets](http://win10widgets.com) - inherits styling from this theme

# Installation

 1. Install [Rainmeter 4.1+](https://www.rainmeter.net) and [Win10Widgets](http://win10widgets.com) if you haven't already
 2. Go to `C:\Users\[MY_USER]\Documents\Rainmeter\Skins\Win10 Widgets` and create a directory called `Cryptometer`
 3. Download the zip from https://github.com/bkuhl/cryptometer and put the contents of the `cryptometer-master` (within the zip file) into the `Cryptometer` directory you just created
 4. Either open Rainmeter or click "Refresh All" in the bottom left corner of the Rainmeter Manager
 
# Managing Cryptocurrencies

Each section of the configuration begins with the currency's name and symbol along with a separator, such as:

```
# Bitcoin (BTC)__________________________________________________________________
```
 
### Removing Cryptocurrencies

 1. Find the section for the currency you'd like to delete
 2. Delete it
 3. Adjust the currencies below it so they move "up a row" visually.  This is done by decrementing the row number after `*` in the `Y` configuration value (e.g. - the number `4` in `Y=(#TopPadding#+(#RowHeight#*4))`)

### Adding Cryptocurrencies

 1. Duplicate an existing currency section
 2. Update the currency name, symbol and necessary URLs (necessary info about currencies can be found in the [CoinMarketCap.com API](https://api.coinmarketcap.com/v1/ticker/)
 3. Adjust the row numbers, positioning the currency on the list where you'd like to see it.  This is done by incrementing or decrementing the row number after `*` in the `Y` configuration value (e.g. - the number `4` in `Y=(#TopPadding#+(#RowHeight#*4))`).  If any numbers have the same rows, they will visually end up in the same space.
 
  > If you have more than 5 currencies, you'll need to adjust `BackgroundHeight=160` in the `[Variables]` section of the file to make sure the widget is tall enough.
