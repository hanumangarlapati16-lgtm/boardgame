pipeline {
    agent any

    tools {
        maven 'maven3.6'  // Define Maven version (configured in Global Tool Configuration)
        jdk 'jdk17'       // Define JDK version (configured in Global Tool Configuration)
    }

    stages {  // The stages block should be here, inside the pipeline block
        stage('Git Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/hanumangarlapati16-lgtm/boardgame.git'
            }
        }

        stage('Compile') {
            steps {
                sh 'mvn compile'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Package') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
