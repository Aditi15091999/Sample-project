pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/python']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Aditi15091999/Sample-project.git']]])
            }
        }
        stage('Build'){
            steps {
                git branch: 'python', url: 'https://github.com/Aditi15091999/Sample-project.git'
                bat 'py list_aditi.py'
            }
        }
        stage('Test'){
            steps {
                echo 'the job has been tested'
            }
        }
    }
}
