pipeline {
    agent any

    tools {
        maven 'Maven'
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'master',
                    url: 'https://github.com/bit-1BI23CS128/prog10.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Run') {
            steps {
                 sh 'java -jar target/MyMavenApp001-1.0-SNAPSHOT.jar'
            }
        }
    }

    post {
        success {
            echo 'Build successful'
        }

        failure {
            echo 'Build failed'
        }
    }
}
