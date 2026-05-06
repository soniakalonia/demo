pipeline {
    agent any

    tools {
        nodejs 'node20'
    }

    stages {

        stage('Checkout') {
            steps {
                git 'https://github.com/soniakalonia/demo.git'
            }
        }

        stage('Install Yarn') {
            steps {
                bat 'npm install -g yarn'
                bat 'yarn config set network-timeout 600000'
                bat 'yarn config set registry https://registry.npmjs.org'
            }
        }

        stage('Install Dependencies') {
            steps {
                bat 'yarn install --network-timeout 600000'
            }
        }

        stage('Build App') {
            steps {
                bat 'yarn build'
            }
        }

        stage('Run Locally') {
            steps {
                bat 'start /B yarn start'
            }
        }
    }
}