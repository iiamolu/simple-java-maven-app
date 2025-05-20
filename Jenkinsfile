pipeline {
    agent any

    tools {
        maven 'Maven 3.9.2'
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
