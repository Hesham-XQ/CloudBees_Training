pipeline {
  agent any
 
    tools {
        maven 'Maven 3.8.4'
        jdk 'jdk8'
    }
  stages {
    stage('Bees Bees update') {
      parallel {
     
    stage ('Initialize') {
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

  }
  environment {
    USER = 'HEsham'
  }
}
