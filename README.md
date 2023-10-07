# Simsimi-Sqlite

## Description

The Simsimi-Sqlite package is a Node.js library that allows you to interact with the SimSimi API for chat and teaching functionalities. It provides convenient methods for making HTTP requests to the SimSimi API and processing the responses.

## Installation

To use the Simsimi-Sqlite package, you can install it using npm:

```bash
npm install Simsimi-Sqlite
```

```javascript
// Import chat and teach functions from Simsimi-Sqlite
const { chat, teach } = require('Simsimi-Sqlite');

(async () => {
  // Testing chat.js
  try {
    const chatResponse = await chat("How are you?");
    console.log("Chat Response:", chatResponse);
    // Access chatResponse.result for chat result
  } catch (error) {
    console.error(error);
  }

  // Testing teach.js
  try {
    const teachResponse = await teach({
      question: "How are you?",
      answer: "I'm fine"
    });
    console.log("Teach Response:", teachResponse);
    // Access teachResponse.asking and teachResponse.answer for teaching result
  } catch (error) {
    console.error(error);
  }
})();

```