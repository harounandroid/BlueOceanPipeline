pipeline {
  agent any
  stages {
    
    stage(' build') {
      steps {
        echo 'build completed'
      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            echo 'testcompleted'
          }
        }

        stage('test2') {
          steps {
            echo 'test2 completed'
          }
        }

        stage('test3') {
          steps {
            echo 'test3 completed'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        echo 'deploy completed'
      }
    }

  }
}
