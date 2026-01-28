pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        sh 'mvn clean package'
      }
    }

    stage('Run') {
      steps {
        sh 'java -jar target/demo-app-1.0-SNAPSHOT.jar || true'
      }
    }
  }
}

