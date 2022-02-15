pipeline {
  agent any
  stages {
    stage('Bees Bees update') {
      parallel {
        stage('Bees Bees update') {
          steps {
            echo 'Buzz, Bees, Buzz!'
            echo ' Bees Buzzing!'
            sh 'echo I am $INVOCATION_ID'
            sh 'echo "artifact test">hello-world.txt'
          }
        }

        stage('parralel 1') {
          steps {
            echo '1'
          }
        }

        stage('parallel 2') {
          steps {
            echo '2'
          }
        }

      }
    }

    stage(' Buzz Build Stage') {
      steps {
        archiveArtifacts(artifacts: '*.txt', allowEmptyArchive: true, fingerprint: true)
      }
    }

  }
  environment {
    USER = 'HEsham'
  }
}