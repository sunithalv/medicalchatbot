# MedicalChatbot

The goal of the project is to create a medical chatbot which can ask questions related to diseases. The data for reference is taken from the The Gale Encyclopedia of Medicine.The LLM model used is https://huggingface.co/TheBloke/Llama-2-7B-Chat-GGML.

## Tech Used
1. Llama2
2. LangChain
3. Pinecone
4. Flask
5. Python


## Run the Application

### Step 1-: Clone the Repository
```
git clone https://github.com/sunithalv/medicalchatbot.git
```

### Step 2-: Create conda environment
```
conda create -n myenv python==3.9 -y
```

### Step 3-: Activate Conda environment
```
conda activate myenv
```

### Step 4-: Install requirements
```
pip install -r requirements.txt
```

### Step 5-: Download the Llama2 model

Download llama-2-7b-chat.ggmlv3.q4_0.bin model from hugging face

### .env file
```
PINECONE_API_KEY= 

PINECONE_ENVIRONMENT= 
```

### Step 6-: Run the application 
```
python store_index.py
python app.py
```
