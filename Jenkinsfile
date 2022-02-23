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

    stage('confirmation!!') {
      steps {
        input(message: 'confirmed ??', ok: 'yes, let\'s do it')
        echo 'WHOOOoooo !!!!'
      }
    }

    stage('Deployment') {
      steps {
        echo "${env.BUILD_ID}"
        echo "${env.executable-war}"
      }
    }

  }
  tools {
    maven 'apache-maven-3.8.4'
  }
  environment {
    USER = 'HEsham'
  }
  post {
    always {
      echo 'I will always say Hello again!'
    }

  }
}