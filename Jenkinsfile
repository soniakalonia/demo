pipeline {
    agent any

    tools {
        nodejs "NodeJS"   // name must match Jenkins NodeJS tool name
    }

    stages {

        stage('Clone Repository') {
            steps {
                git branch: 'main',
                url: 'https://github.com/soniakalonia/demo.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                bat 'npm install'
            }
        }

        stage('Run React App') {
            steps {
                bat 'npm run dev'
            }
        }
    }
}