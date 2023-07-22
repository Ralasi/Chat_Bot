# Chat_Bot

SCREENSHOT :
![Screenshot (280)](https://github.com/Ralasi/Chat_Bot/assets/128724283/fa965d1c-30bc-4f7d-aaef-72005f4d20aa)

CLICK TO VISIT DEMO VIDEO
[DEMO VIDEO](https://drive.google.com/file/d/1C7yQqFzsV92h3t8yIAGNOM6EEl7be0No/view?usp=sharing)

LANGUAGE AND TECHNOLOGY :
HTML, CSS, JavaScript, API(Open AI)

Explanation of the code:

1. The code starts by selecting various elements from the DOM using query selectors. These elements include the chatbot toggler, close button, chatbox, chat input textarea, and send chat button.

2. The variable `userMessage` is initialized as null. It will be used to store the user's message later.

3. The `API_KEY` constant is set to a specific value. This key is used for authentication when making API requests.

4. The `inputInitHeight` variable is set to the scroll height of the chat input textarea. It represents the initial height of the textarea.

5. The `createChatLi` function is defined. It takes a message and a className as parameters and creates a chat `<li>` element with the provided message and className. The className is used to determine if the chat is outgoing or incoming.

6. The `generateResponse` function is defined. It takes a chat element as a parameter. Inside the function, an API request is made to the OpenAI API using the provided API key and user's message. The response from the API is then set as the text content of the chat element.

7. The `handleChat` function is defined. It is responsible for handling user input and generating a response. First, it trims the user's message and stores it in the `userMessage` variable. If the message is empty, the function returns early. Otherwise, it clears the chat input textarea and sets its height to the default value. Then, it appends the user's message as an outgoing chat to the chatbox. After a short delay, it appends an incoming chat with the text "Thinking..." to indicate that the chatbot is processing the response. Finally, it calls the `generateResponse` function to generate the actual response based on the user's message.

8. Event listeners are added to the chat input textarea and send chat button. The input event listener adjusts the height of the textarea based on its content. The keydown event listener checks if the Enter key is pressed without the Shift key and the window width is greater than 800 pixels. If these conditions are met, it prevents the default behavior (which would insert a new line) and calls the `handleChat` function. The click event listener on the send chat button also calls the `handleChat` function.

9. Event listeners are added to the close button and chatbot toggler. The click event listener on the close button removes the "show-chatbot" class from the document body, hiding the chatbot. The click event listener on the chatbot toggler toggles the "show-chatbot" class on the document body, showing or hiding the chatbot based on its current state.
