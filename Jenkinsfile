pipeline {
    agent any 
    
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Renu-Kumar-M/jenkins-app.git'
            }
        }
        
        stage('Install Dependencies') {
            steps {
                bat 'pip install -r requirements.txt'
            }
        }
        
        stage('Run Unit Tests') {
            steps {
                bat 'pytest test_app.py'
            }
        }
    }
}
