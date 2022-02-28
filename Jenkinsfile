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
      agent {
        node {
          label 'xq'
        }

      }
      steps {
        input(message: 'confirmed ??', ok: 'yes, let\'s do it')
        echo 'WHOOOoooo !!!!'
      }
    }

    stage('Deployment') {
      steps {
        echo "${env.BUILD_ID}"
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
      emailext(subject: "SUCCESSFUL: Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]'", body: """<p>SUCCESSFUL: Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]':</p>
                                            <p>Check console output at &QUOT;<a href='${env.BUILD_URL}'>${env.JOB_NAME} [${env.BUILD_NUMBER}]</a>&QUOT;</p>""", to: 'hesham001230@gmail.com')
    }

  }
}