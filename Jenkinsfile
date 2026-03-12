pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/ArsalaanS/comp367-maven-app.git'
            }
        }
        stage('Build') {
            steps {
                bat 'mvn compile'
            }
        }
        stage('Run') {
            steps {
                bat 'mvn exec:java -Dexec.mainClass="com.centennial.App"'
            }
        }
    }
}