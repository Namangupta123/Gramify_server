## Description
The `server.js` file contains the backend logic for a grammar correction assistant API using the MistralAI model. It utilizes Express for handling HTTP requests and responses.

### Setup
1. Install dependencies by running `npm install`.
2. Create a `.env` file and add your Mistral API key as `MISTRAL_API_KEY=your_api_key_here`.
3. Start the server by running `node server.js`.

### API Endpoints
- `POST /fix-grammer`: 
  - Description: Corrects grammar mistakes in the provided text.
  - Request Body: 
    ```
    {
        "text": "Text to be corrected"
    }
    ```
  - Response:
    ```
    {
        "correctedText": "Corrected text"
    }
    ```
- `GET /`:
  - Description: Returns a status message indicating the server is running.

### Error Handling
- If no text is provided in the request body for `/fix-grammer`, a `400` status with an error message will be returned.
- If there is an internal server error, a `500` status with an error message will be returned.

### Dependencies
- Express
- Cors
- Dotenv
- @langchain/mistralai
- @langchain/core/prompts

### Environment Variables
- `MISTRAL_API_KEY`: API key for the MistralAI model.

### Usage
You can send a POST request to `/fix-grammer` with a JSON body containing the text to be corrected.

### Contributions

We welcome contributions to improve this grammar correction assistant API. Feel free to submit pull requests with enhancements, bug fixes, or new features.

