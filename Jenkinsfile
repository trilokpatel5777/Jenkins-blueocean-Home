pipeline {
  agent any
  stages {
    stage('test') {
      steps {
        echo 'test'
      }
    }

    stage('build') {
      parallel {
        stage('build') {
          steps {
            bat 'echo "%date%"'
          }
        }

        stage('build-parallel') {
          steps {
            echo 'parallel'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        echo 'deploy'
      }
    }

    stage('continue?') {
      steps {
        input(message: 'continue?', ok: 'yes continue')
      }
    }

  }
}