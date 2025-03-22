# WebDev-AI-Recruiter: Flask + React Application
WebDev AI Recruiter integrates advanced AI models to match job descriptions with resumes, facilitating an automated recruitment process. Built with Flask and React, this application offers a user-friendly interface and efficient backend services.

# Table of Contents
- Getting Started
  - Server Setup
   - Client Setup
- Important Links
  - Datasets
  - Model
- Project Tasks
- Deployment
  - Flask Application
  - React Application

## Getting Started
**Server Setup**

Set up the Flask backend:

    cd server
    virtualenv env
    env\Scripts\activate
    pip install -r requirements.txt
    flask run
    
**Client Setup**

Set up the Vite + React frontend (ensure Node.js is installed):

    cd client
    npm install --legacy-peer-deps
    npm run dev

## Important Links
Links to datasets used for training AI models:
**1. job description in indonesian :** https://www.kaggle.com/datasets/canggih/jog-description-and-salary-in-indonesia

**2. it job description :** https://www.kaggle.com/datasets/mscgeorges/itjobpostdescriptions?resource=download

**3. resume 1 :** https://www.kaggle.com/datasets/gauravduttakiit/resume-dataset

**4. resume 2 :** https://huggingface.co/datasets/InferencePrince555/Resume-Dataset

**5. job description - resume pair :** https://huggingface.co/datasets/cnamuangtoun/resume-job-description-fit 

## Model
https://huggingface.co/bwbayu/sbert_model_jobcv/tree/main

## Project Tasks
- CI/CD: Continuous integration and deployment.
- Domain Configuration: Manage custom domain settings.

## Deployment
Deploy the Flask app using Google Cloud Run:

    create Dockerfile and .dockerignore
    gcloud init
    gcloud run deploy --source .

- **Configure environment variables and memory settings in the Cloud Run dashboard**
  - setting env -> service detail -> edit & deploy new revision -> variables & secrets
  - update memory -> service detail -> edit & deploy new revision -> resources

## React Application
Deploy the React app on Google Cloud Run:

    npm run build
    create Dockerfile, .dockerignore, nginx.conf
    gcloud init
    gcloud run deploy --source .

## Contributing
For contributions, please fork the repository, create a feature branch, and submit a pull request.

## License
This project is licensed under the MIT License - see the LICENSE file for details.
