# R-C-Chatbot

This Streamlit application allows users to upload `.txt`, `.pdf`, and `.docx` files, and ask questions about the contents of those documents. It uses Together AI's language model for question answering (QA) tasks.

## Features
- **File Upload**: Supports text, PDF, and Word files.
- **Automatic Loading**: Loads a default file (`FD.docx`) automatically, if available.
- **Document Splitting**: Splits large documents into manageable chunks for better processing.
- **Chat History**: Displays a history of user questions and AI responses.
- **Custom Questions**: Allows users to ask specific questions about the uploaded documents.

## Requirements

To run this application, ensure you have the following installed:

- Python 3.8+
- Streamlit
- Together AI SDK (`langchain-together`)
- Required Python libraries: 
  - `langchain`
  - `PyPDF2`
  - `docx`

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/your-repo-name
   cd your-repo-name
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Add your Together AI API key to the `secrets.toml` file in your Streamlit configuration:
   ```toml
   [together_ai]
   api_key = "YOUR_API_KEY"
   model = "MODEL_NAME"  # e.g., "together-gpt-3.5-turbo"
   ```

## Usage

1. Run the Streamlit app:
   ```bash
   streamlit run app.py
   ```

2. Upload your `.txt`, `.pdf`, or `.docx` files using the file uploader.

3. Ask questions about the uploaded content using the input box provided.

4. View the assistant's responses and chat history for reference.

## File Handling

### Supported Formats
- Plain text (`.txt`)
- PDF (`.pdf`)
- Microsoft Word (`.docx`)

### Document Splitting
Large documents are split into smaller chunks using a recursive character text splitter. Chunk size and overlap can be configured for better context management.

## Troubleshooting
- Ensure all required libraries are installed.
- Verify your Together AI API key and model name are correctly configured in `secrets.toml`.
- For unsupported file types, ensure files are in one of the supported formats.

## Contributing
Contributions are welcome! Feel free to open issues or submit pull requests to improve the app.

## License
This project is licensed under the MIT License.

## Acknowledgments
- [Together AI](https://www.together.xyz/) for their language models.
- [Streamlit](https://streamlit.io/) for the intuitive web app framework.

---

Enjoy using the File Q&A application! 🚀