#### This solution was inspire from: https://github.com/imartinez/privateGPT and https://github.com/jmorganca/ollama

#### Step 1: Step a Virtual Environment

#### Step 2: Install the Requirements
```
pip install -r requirements.txt
```

#### Step 3: Pull the models (if you already have models loaded in Ollama, then not required)
#### Make sure to have Ollama running on your system from https://ollama.ai
```
ollama pull mistral
```

#### Step 4: put your files in the source_documents folder after making a directory
```
mkdir source_documents
```

#### Step 5: Ingest the files (use python3 if on mac)
```
python alpaca-ingest.py
```

Output should look like this:
```shell
Creating new vectorstore
Loading documents from source_documents
Loading new documents: 100%|██████████████████████| 1/1 [00:01<00:00,  1.99s/it]
Loaded 235 new documents from source_documents
Split into 1268 chunks of text (max. 500 tokens each)
Creating embeddings. May take some minutes...
Ingestion complete! You can now run privateGPT.py to query your documents
```

#### Step 6: Run this command (use python3 if on mac)
```
python python alpaca-bot.py
```
### Step 7: enter a query 