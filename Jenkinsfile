pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        sh 'mvn clean package'
      }
    }

    stage('Deploy') {
      steps {
        sh '''
          echo "Deploying app"
          mkdir -p /opt/app
          cp target/demo-app-1.0-SNAPSHOT.jar /opt/app/
          echo "Done"
        '''
      }
    }
  }
}
