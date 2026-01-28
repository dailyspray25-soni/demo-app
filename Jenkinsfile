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
          mkdir -p /home/ubuntu/app
          cp target/demo-app-1.0-SNAPSHOT.jar /home/ubuntu/app/
          echo "Deployment complete"
        '''
      }
    }
  }
}
