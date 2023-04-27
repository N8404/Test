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
      }
      
      /* Add a blue border to the message input area */
      #message-input {
        border: 2px solid blue;
        padding: 10px;
        width: 100%;
      }
    </style>
  </head>
  <body>
    <div id="chat-window">
      <h1>Chat Room</h1>
      
      <div id="chat-messages">
        <!-- Chat messages will be displayed here -->
      </div>
      
      <form id="chat-form">
        <input type="text" id="message-input" placeholder="Type your message...">
        <button type="submit">Send</button>
      </form>
    </div>
    
    <script>
      const chatWindow = document.getElementById("chat-window");
      const chatMessages = document.getElementById("chat-messages");
      const chatForm = document.getElementById("chat-form");
      const messageInput = document.getElementById("message-input");
      
      // Function to add a new chat message to the chat window
      function addMessage(message) {
        const messageElement = document.createElement("div");
        messageElement.innerText = message;
        chatMessages.appendChild(messageElement);
      }
      
      // Function to handle the chat form submission
      function handleSubmit(event) {
        event.preventDefault();
        const message = messageInput.value;
        messageInput.value = "";
        addMessage(message);
      }
      
      // Attach the event listener for form submission
      chatForm.addEventListener("submit", handleSubmit);
    </script>
  </body>
</html>
