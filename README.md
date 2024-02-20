# MedicalChatbot

The goal of the project is to create a medical chatbot which can identify diseases and prescribe medicines based on the symptoms provided. The data for reference is taken from the The Gale Encyclopedia of Medicine

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

### Step 5-: Export the environment variable
```
export SECRET_KEY=<SECRET_KEY>

export ALGORITHM=<ALGORITHM>

export MONGODB_URL_KEY=<MONGODB_URL_KEY>

export DATABASE_NAME=<DATABASE_NAME>

export USER_COLLECTION_NAME=<USER_COLLECTION_NAME>

export EMBEDDING_COLLECTION_NAME=<EMBEDDING_COLLECTION_NAME>
```
### .env file
```
SECRET_KEY=KlgH6AzYDeZeGwD288to79I3vTHT8wp7
ALGORITHM=HS256
DATABASE_NAME='UserDatabase'
USER_COLLECTION_NAME='User'
EMBEDDING_COLLECTION_NAME='Embedding'
MONGODB_URL_KEY=
```

### Step 6-: Run the application server
```
python app.py
```

## Run Locally

### Build the Docker Image
```
docker build -t face_auth --build-arg SECRET_KEY=<SECRET_KEY> --build-arg ALGORITHM=<ALGORITHM> --build-arg MONGODB_URL_KEY=<MONGODB_URL_KEY> --build-arg DATABASE_NAME=<DATABASE_NAME> --build-arg USER_COLLECTION_NAME=<USER_COLLECTION_NAME> --build-arg EMBEDDING_COLLECTION_NAME=<EMBEDDING_COLLECTION_NAME> . 
```

### Run the Docker Image

```
docker run -d -p 8000:8000 <IMAGEID OR IMAGENAME>
```
## Deployment to Azure

### Services used
- Azure container Registry (ACR) for Docker image of project is stored
- Azure App Services for deploying the application
- GitHub Actions for CI/CD



