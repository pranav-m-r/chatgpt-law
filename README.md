# Law Chatbot

The project uses the dropbox chatbot template to train the gpt model on important bills passed by the Indian government after the training cutoff of OpenAI's GPT 3.5 model. Law documents are important documents for any citizen of the country, but also are the most difficult to read and comprehend for a civilian. So this tool can serve as a useful resource for anyone who wants to learn about the new laws passed and how it impacts them.

## Demo

See how the tool works:

![Dropbox AI search tool demo](assets/dropbox-ai-search-tool.gif)

As you can see the LLM App enables AI-powered search from multiple unstructured documents like tax information from different countries, and indexes input data in real-time just after you upload files to the cloud storage.

## Run with Docker

1. Create `.env` file in the root directory of the project, copy and paste the below config. Replace the `OPENAI_API_TOKEN` configuration value with your key `{OPENAI_API_KEY}` and replace `DROPBOX_LOCAL_FOLDER_PATH` with a path where Dropbox folder is located `{REPLACE_WITH_DROPBOX_FOLDER_PATH}`. For example, if the current project folder is `DROPBOX-SEARCH-TOOL`, you navigate to the Dropbox path in the home directory: `../Dropbox/documents`. Other properties are optional to change and be default.

```bash
OPENAI_API_TOKEN={OPENAI_API_KEY}
EMBEDDER_LOCATOR=text-embedding-ada-002
EMBEDDING_DIMENSION=1536
MODEL_LOCATOR=gpt-3.5-turbo
MAX_TOKENS=500
TEMPERATURE=0.0
DROPBOX_LOCAL_FOLDER_PATH={REPLACE_WITH_DROPBOX_RELATIVE_PATH}
```

2. From the project root folder, open your terminal and run `docker compose up`.
3. Navigate to `localhost:8501` on your browser when docker installion is successful.