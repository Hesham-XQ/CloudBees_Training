pipeline {
  agent any
  stages {
    stage('Bees Bees update') {
      steps {
        echo 'Buzz, Bees, Buzz!'
        echo ' Bees Buzzing!'
        sh 'pwd'
        sh 'echo "Bees Buzzing Again">hello-world.txt'
      }
    }

    stage(' Buzz Build Stage') {
      steps {
        archiveArtifacts(artifacts: '/*.txt', allowEmptyArchive: true, fingerprint: true)
      }
    }

  }
}