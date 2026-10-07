pipeline {
    agent any
    tools {
        maven 'Maven3'
    }
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/ganeshkumars2024-ai/maven_project1.git'
            }
        }
        stage('Package') {
            steps {
                bat 'mvn clean package'
            }
        }
        stage('Run JAR') {
            steps {
                bat 'java -cp target\\maven-package-demo-1.0.jar com.example.App'
            }
        }
    }
}
