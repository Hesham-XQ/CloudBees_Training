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
        archiveArtifacts(artifacts: '/var/lib/jenkins/test/*.jar', allowEmptyArchive: true, fingerprint: true)
      }
    }

  }
}