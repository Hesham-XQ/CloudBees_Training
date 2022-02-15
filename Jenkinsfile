pipeline {
  agent any
  stages {
    stage('Bees Bees update') {
      steps {
        echo 'Buzz, Bees, Buzz!'
        echo ' Bees Buzzing!'
        sh 'echo I am $INVOCATION_ID'
        sh 'echo "Bees Buzzing Again">hello-world.txt'
      }
    }

    stage(' Buzz Build Stage') {
      steps {
        archiveArtifacts(artifacts: '*.txt', allowEmptyArchive: true, fingerprint: true)
        junit(testResults: '**/surefire-reports/**/*.xml', allowEmptyResults: true)
      }
    }

  }
  environment {
    USER = 'HEsham'
  }
}