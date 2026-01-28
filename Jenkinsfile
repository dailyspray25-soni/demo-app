pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'echo BUILD_STARTED'
                sh 'mvn clean package'
                sh 'echo BUILD_FINISHED'
            }
        }

        stage('Run') {
            steps {
                sh 'java -jar target/demo-app-1.0-SNAPSHOT.jar || true'
            }
        }
    }
}

