pipeline {
    agent any
    stages {
        stage('Build & Run') {
            steps {
                // Checkout the main branch only once
                git branch: 'main', url: 'https://github.com/ArsalaanS/comp367-maven-app.git'

                // Compile and run Maven project
                sh 'mvn compile'
                sh 'mvn exec:java -Dexec.mainClass="com.centennial.App"'
            }
        }
    }
}