# Nodebot

An application to control a mBot using Node. This application give an HCI
to control the mBot from the browser.

## Instructions

The application can be divided into two part: the `frontend` and the `backend`.
The `backend` must serves the `frontend` app and gives an API to control the mBot.
And the `frontend` must be an HCI giving the user a visual way to control the mBot.

### The Backend

Here are some guidance to build the backend application:

1. install `Express` using `npm`
2. create a `public` folder and serve the public folder using `Express`
3. at this step the frontend developpement can start 
4. create a new file `bot.js` which register 5 routes:
    - `/bot/left` which answer `GET` request and makes the bot turn left
    - `/bot/right` which answer `GET` request and makes the bot turn right
    - `/bot/forward` which answer `GET` request and makes the bot go forward
    - `/bot/backward` which answer `GET` request and makes the bot go backward
    - `/bot/stop` which answer `GET` request and stops the bot

### The Frontend

Here are some guidance to build the frontend application:

1. create a new page `index.html` with:
    - 4 buttons to control the bot (left, forward, backward, right)
    - 1 button to stop the bot
2. add a `script` element to the page which listen for `click` event on each button
and make the appropriate AJAX request to the bot API:
    - the button `forward` should send a `GET` request to `/bot/forward`
    - the button `backward` should send a `GET` request to `/bot/backward`
    - etc...
3. add a `script` element to the page which listen for keyboard event and control the bot using the keyboard arrow (or `z`, `q`, `s`, `d`)