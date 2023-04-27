<!DOCTYPE html>
<html>
  <head>
    <title>Chat Room</title>
    <style>
      /* Center the chat window */
      body {
        display: flex;
        justify-content: center;
        align-items: center;
        height: 100vh;
      }
      
      /* Add a thick blue border to the chat window */
      #chat-window {
        border: 5px solid blue;
        padding: 20px;
        width: 500px;
        max-height: calc(100vh - 150px);
        overflow-y: scroll;
      }
      
      /* Add a blue border to the message input area */
      #message-input {
        border: 2px solid blue;
        padding: 10px;
        width: 100%;
      }
      
      /* Add a gray background to the login form popup */
      #login-popup {
        display: flex;
        justify-content: center;
        align-items: center;
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background-color: rgba(0, 0, 0, 0.5);
        z-index: 1;
        visibility: hidden;
      }
      
      /* Add a white background and padding to the login form */
      #login-form {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        width: 300px;
        height: 200px;
        background-color: white;
        padding: 20px;
        border-radius: 10px;
      }
      
      /* Add styles to the login form elements */
      #login-form label, #login-form input, #login-form button {
        margin-bottom: 10px;
        font-size: 18px;
      }
      
      #login-form label {
        font-weight: bold;
      }
      
      #login-form input[type="text"], #login-form input[type="password"] {
        width: 100%;
        padding: 10px;
        font-size: 16px;
        border: 1px solid gray;
        border-radius: 5px;
      }
      
      #login-form button {
        background-color: blue;
        color: white;
        padding: 10px;
        border: none;
        border-radius: 5px;
        cursor: pointer;
      }
      
      /* Add a border around the username display */
      #username-display {
        border: 2px solid blue;
        padding: 10px;
        margin-bottom: 10px;
      }
    </style>
  </head>
  <body>
    <div id="login-popup">
      <form id="login-form">
        <label for="username-input">Username:</label>
        <input type="text" id="username-input" required>
        <label for="password-input">Password:</label>
        <input type="password" id="password-input" required>
        <button type="submit">Log in</button>
      </form>
    </div>
    
    <div id="chat-window">
      <div id="username-display"></div>
      <h1>Chat Room</h1>
      
      <div id="chat-messages">
        <!-- Chat messages will be displayed here -->
      </div>
    </div>
    
    <form id="chat-form">
      <input type="text" id="message-input" placeholder="Type your message...">
      <button type="submit">Send</button>
    </form>

