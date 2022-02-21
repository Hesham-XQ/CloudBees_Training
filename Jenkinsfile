pipeline {
  agent any
  stages {
    stage('Bees Bees update') {
      parallel {
        stage('Initialize') {
          steps {
            sh '''
                echo "PATH = ${PATH}"
                echo "M2_HOME = ${M2_HOME}"
            '''
          }
        }

        stage('Bees Bees update') {
          steps {
            echo 'Buzz, Bees, Buzz!'
            echo ' Bees Buzzing!'
            sh 'echo I am $INVOCATION_ID'
            sh 'echo "Bees Buzzing Again">hello-world.txt'
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
        junit(testResults: '**/surefire-reports/**/*.xml', allowEmptyResults: true)
      }
    }

    stage('confirmation!!') {
      steps {
        input(message: 'confirmed ??', ok: 'yes, let\'s do it')
        echo 'WHOOOoooo !!!!'
      }
    }

    stage('Deployment') {
      steps {
        sh 'deploy.sh'
      }
    }

  }
  tools {
    maven 'apache-maven-3.8.4'
  }
  environment {
    USER = 'HEsham'
  }
}