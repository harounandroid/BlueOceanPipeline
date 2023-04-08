pipeline {
  agent any
  stages {
    stage('Branch indexing: abort') {
            when {
                allOf {
                    triggeredBy cause: "BranchIndexingCause"
                    not { 
                        changeRequest() 
                    }
                }
            }
            steps {
                script {
                    echo "Branch discovered by branch indexing"
                    currentBuild.result = 'SUCCESS' 
                    error "Caught branch indexing..."
                }
            }
        }
    
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
