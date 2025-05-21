# DeepSeek AI Chatbot

A simple, elegant chatbot application that integrates with the DeepSeek AI API to create an interactive conversational experience. Built with Node.js, Express.js, and EJS.


## Features

- Clean, modern chat interface
- Real-time conversation with AI
- Loading indicators for better user experience
- Mobile-responsive design
- Easy customization options

## Prerequisites

Before you start, you'll need:

- [Node.js](https://nodejs.org/) (v14.0.0 or higher)
- [npm](https://www.npmjs.com/) (normally comes with Node.js)
- [DeepSeek API Key](https://platform.deepseek.com/)

## Installation

1. **Clone the repository or download the source code**

   ```bash
   git clone https://github.com/yourusername/deepseek-chatbot.git
   cd deepseek-chatbot
   ```

   Or simply download and extract the ZIP file.

2. **Install dependencies**

   ```bash
   npm install
   ```

3. **Create a .env file**

   Create a `.env` file in the root directory and add your DeepSeek API key:

   ```
   PORT=3000
   DEEPSEEK_API_KEY=your_deepseek_api_key_here
   ```

   Replace `your_deepseek_api_key_here` with your actual DeepSeek API key.

## Getting a DeepSeek API Key

1. Sign up for an account at [DeepSeek Platform](https://platform.deepseek.com/)
2. After verifying your account, navigate to your profile or API settings
3. Generate a new API key
4. Copy the key and paste it into your `.env` file

## Running the Application

1. **Start the server**

   ```bash
   npm start
   ```

   Or, for development with auto-restart:

   ```bash
   npm run dev
   ```

2. **Open your browser**

   Navigate to [http://localhost:3000](http://localhost:3000) to see the chatbot in action.

## Usage

1. Type your message in the input field at the bottom of the chat interface
2. Press Enter or click the Send button to send your message
3. The chatbot will process your message and respond through the DeepSeek AI API
4. Continue the conversation as long as you want!

## DeepSeek API Usage Notes

- The free tier on DeepSeek has certain limitations, including:
  - Daily request quotas
  - Token limitations per request
  - Model access restrictions
- You may need to upgrade to a paid plan for production use
- Keep your API key secure and don't expose it in client-side code

## Customization

### Changing the AI Model

You can modify the model used in the `app.js` file:

```javascript
const response = await axios.post(
  'https://api.deepseek.com/v1/chat/completions',
  {
    model: 'deepseek-chat', // Change this to another available model
    messages: [
      { role: 'user', content: message }
    ],
    temperature: 0.7, // Adjust for more creative (higher) or deterministic (lower) responses
    max_tokens: 500 // Adjust maximum response length
  },
  // ...
);
```

### Styling

Modify the CSS in `public/css/style.css` to change the appearance of the chatbot.

## Project Structure

```
deepseek-chatbot/
├── app.js               # Main application file
├── .env                 # Environment variables (create this)
├── package.json         # Dependencies and scripts
├── public/              # Static files
│   ├── css/
│   │   └── style.css    # Chatbot styling
│   └── js/
│       └── main.js      # Frontend JavaScript
└── views/
    └── index.ejs        # Chat interface template
```

## Troubleshooting

### "Insufficient Balance" Error

If you receive an "Insufficient Balance" error, it means your DeepSeek account doesn't have enough credits. You can:

1. Check your DeepSeek dashboard for usage statistics
2. Look for any free credit offers or promotions
3. Upgrade to a paid plan if needed
4. Contact DeepSeek support for assistance

### Other Common Issues

- **Connection Failed**: Ensure your internet connection is stable
- **Invalid API Key**: Double-check your API key in the `.env` file
- **Rate Limiting**: DeepSeek may limit requests; add delay between messages
- **Model Loading**: Some models may take time to load on first request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- [DeepSeek](https://deepseek.com/) for providing the AI API
- [Express.js](https://expressjs.com/) for the web framework
- [EJS](https://ejs.co/) for the templating engine

---

Made with ❤️ by Rizky Nugraha Amaia
```

If you need more help or have questions, feel free to reach out!