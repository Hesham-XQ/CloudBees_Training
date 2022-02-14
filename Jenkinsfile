pipeline {
  agent any
  stages {
    stage('Bees Bees update') {
      steps {
        echo 'Buzz, Bees, Buzz!'
        echo ' Bees Buzzing!'
        sh 'pwd'
        echo 'Bees Buzzing Again'
      }
    }

    stage(' Buzz Build Stage') {
      steps {
        sh './jenkins/build.sh'
      }
    }

    stage('Buzz Test') {
      steps {
        sh './jenkins/test-all.sh'
      }
    }

  }
}