pipeline {
    agent any

    tools {
        maven 'Maven 3.8.1'
    }

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/iiamolu/simple-java-maven-app.git'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage('Archive') {
            steps {
                archiveArtifacts artifacts: 'target/*.jar', fingerprint: true
            }
        }
    }
}
