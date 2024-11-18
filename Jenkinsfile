pipeline {
    
    agent any

    stages {
        stage('Code') {
            steps {
                git url:"https://github.com/rutujachandurkar03/Django-to-do.git",branch:"master"
                  }
                    }
        stage('Build'){
            steps {
                sh "docker build -t django-to-do ."
            }
        }
        stage('Deploy'){
            steps {
                sh 'docker run -d -p 8000:8000 django-to-do:latest'
            }
        }
        
    }
}
                
