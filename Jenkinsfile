pipeline {
    agent any

    tools {
        nodejs 'node18'
    }

    stages {

        stage('Clone Code') {
            steps {
                git 'https://github.com/soniakalonia/demo.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                bat 'npm install'
            }
        }

        stage('Build React App') {
            steps {
                bat 'npm run build'
            }
        }

        stage('Serve Build Locally') {
            steps {
                bat 'npm install -g serve'
                bat 'serve -s dist -l 3000'
            }
        }
    }
}