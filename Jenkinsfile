pipeline {
    agent any

    tools {
        nodejs 'node18'
    }

    stages {

        stage('Install Yarn') {
            steps {
                bat 'npm install -g yarn'
            }
        }

        stage('Install Dependencies') {
            steps {
                bat 'yarn install'
            }
        }

        stage('Build React App') {
            steps {
                bat 'yarn build'
            }
        }

        stage('Serve Build Locally') {
            steps {
                bat 'npm install -g serve'
                bat 'serve -s apps/react-vite/dist -l 3000'
            }
        }
    }
}