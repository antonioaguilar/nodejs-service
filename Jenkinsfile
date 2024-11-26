pipeline {
  agent any

  stages {

    stage('Build') {
      parallel {
        stage('Build service') {
          steps {
             sh 'sleep 3s'
          }
        }
        stage('Build container image') {
          steps {
             sh 'sleep 5s'
          }
        }
      }
    }

    stage('Test') {
      parallel {
        stage('Unit Tests') {
          steps {
             sh 'sleep 3s'
          }
        }
        stage('Integration Tests') {
          steps {
             sh 'sleep 4s'
          }
        }
        stage('SonarQube Coverage') {
          steps {
             sh 'sleep 6s'
          }
        }
      }
    }

    stage('Performance') {
      parallel {
        stage('E2E Cypress Tests') {
          steps {
             sh 'sleep 6s'
          }
        }
        stage('Postman REST Tests') {
          steps {
             sh 'sleep 3s'
          }
        }
        stage('K6 Load Tests') {
          steps {
             sh 'sleep 6s'
          }
        }
        stage('JMeter/BlazeMeter Tests') {
          steps {
             sh 'sleep 5s'
          }
        }
        stage('Regresion Testing (automated)') {
          steps {
             sh 'sleep 7s'
          }
        }
      }
    }

    stage('Security') {
      parallel {
        stage('SAST Scanning') {
          steps {
             sh 'sleep 2s'
          }
        }
        stage('Semgrep CVE audits') {
          steps {
             sh 'sleep 4s'
          }
        }
        stage('Artifactory SCA Scanning') {
          steps {
             sh 'sleep 5s'
          }
        }
        stage('SBOM generation') {
          steps {
             sh 'sleep 7s'
          }
        }
        stage('Container Image Scanning (SBOM)') {
          steps {
             sh 'sleep 10s'
          }
        }
      }
    }

    stage('Compliance') {
      parallel {
        stage('SBOM Report') {
          steps {
             sh 'sleep 2s'
          }
        }
        stage('License Scanning') {
          steps {
             sh 'sleep 4s'
          }
        }
        stage('API Documentation') {
          steps {
             sh 'sleep 5s'
          }
        }
      }
    }

    stage('Release') {
      parallel {
        stage('Artifactory Upload') {
          steps {
             sh 'sleep 3s'
          }
        }
        stage('SBOM Report') {
          steps {
             sh 'sleep 5s'
          }
        }
        stage('Artifact Report') {
          steps {
             sh 'sleep 7s'
          }
        }
      }
    }

    stage('Deploy') {
      parallel {
        stage('Deploy to Staging env') {
          steps {
             sh 'sleep 3s'
          }
        }
        stage('Deploy to QA env') {
          steps {
             sh 'sleep 3s'
          }
        }
      }
    }

  }
}
