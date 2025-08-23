# Project Setup Guide

## Create Project Folder and Environment Setup

```bash
# Create a new project folder
mkdir <project_folder_name>

# Move into the project folder
cd <project_folder_name>

# Open the folder in VS Code
code .

# Create a new Conda environment with Python 3.10
conda create -p <env_name> python=3.10 -y

# Activate the environment (use full path to the environment)
conda activate <path_of_the_env>

# Install dependencies from requirements.txt
pip install -r requirements.txt

# Initialize Git
git init

# Stage all files
git add .

# Commit changes
git commit -m "<write your commit message>"

# Push to remote (after adding remote origin)
git push

# Cloning the repository
git clone https://github.com/sunnysavita10/document_portal.git
```
## Minimum Requirements for the Project

### LLM Models
- **Groq** (Free)
- **OpenAI** (Paid)
- **Gemini** (15 Days Free Access)
- **Claude** (Paid)
- **Hugging Face** (Free)
- **Ollama** (Local Setup)

### Embedding Models
- **OpenAI**
- **Hugging Face**
- **Gemini**

### Vector Databases
- **In-Memory**
- **On-Disk**
- **Cloud-Based**

## API Keys

### GROQ API Key
- [Get your API Key](https://console.groq.com/keys)  
- [Groq Documentation](https://console.groq.com/docs/overview)

### Gemini API Key
- [Get your API Key](https://aistudio.google.com/apikey)  
- [Gemini Documentation](https://ai.google.dev/gemini-api/docs/models)


https://hub.docker.com/layers/sunnysavita1095/document-portal-app/latest/images/sha256-ac61ae1c8766a6c7d4de6f8d9a97279c95c0e3302a1d591548ce467a8a6c9d29

login to dockerhub and search name sunnysavita1095 
docker container is nothing but an isolated machine inside system or virtual machine and it is linux based machine/environment
docker build -t my-document-portal:latest .
docker compose concept
as of now logs in our application all logs goes to container
docker compose is a very important concept
docker run -d -p 8093:8080 --name doc-portal my-document-portal:latest
CMD ["uvicorn", "api.main:app", "--host", "0.0.0.0", "--port", "8080", "--reload"]
docker run -d -p 8080:8080 --name alam-doc-portal doc-portal:latest

aws cloudformation deploy --template-file template.yml --stack-name doc-analysis-stack --capabilities CAPABILITY_NAMED_IAM


Setup is done for unit test cases
You have to write at least 10 unit test cases inside test folder > unit_test.py
optional explore integration test cases

After pushing the code over the github we are runing our test cases;
Precommit test cases
