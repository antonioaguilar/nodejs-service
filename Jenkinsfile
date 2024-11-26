pipeline {
  agent any

  stages {

    stage('Build') {
      parallel {
        stage('Build service') {
          steps {
             echo ''
          }
        }
        stage('Build container image') {
          steps {
             echo ''
          }
        }
      }
    }

    stage('Test') {
      parallel {
        stage('Unit Tests') {
          steps {
             echo ''
          }
        }
        stage('Integration Tests') {
          steps {
             echo ''
          }
        }
        stage('SonarQube Coverage') {
          steps {
             echo ''
          }
        }
      }
    }

    stage('Performance') {
      parallel {
        stage('E2E Cypress Tests') {
          steps {
             echo ''
          }
        }
        stage('Postman REST Tests') {
          steps {
             echo ''
          }
        }
        stage('K6 Load Tests') {
          steps {
             echo ''
          }
        }
        stage('JMeter/BlazeMeter Tests') {
          steps {
             echo ''
          }
        }

        stage('Regresion Testing (automated)') {
          steps {
             echo ''
          }
        }
      }
    }

    stage('Compliance & Security') {
      parallel {
        stage('SAST Scanning') {
          steps {
             echo ''
          }
        }
        stage('Semgrep CVE audits') {
          steps {
             echo ''
          }
        }
        stage('Artifactory SCA Scanning') {
          steps {
             echo ''
          }
        }
        stage('License Scanning') {
          steps {
             echo ''
          }
        }
        stage('SBOM generation') {
          steps {
             echo ''
          }
        }
        stage('Container Image Scanning (SBOM)') {
          steps {
             echo ''
          }
        }
      }
    }

    stage('Release') {
      parallel {
        stage('Artifactory Upload') {
          steps {
             echo ''
          }
        }
        stage('SBOM Report') {
          steps {
             echo ''
          }
        }
        stage('Artifact Report') {
          steps {
             echo ''
          }
        }
      }
    }

    stage('Deploy') {
      parallel {
        stage('Deploy to Staging env') {
          steps {
             echo ''
          }
        }
        stage('Deploy to QA env') {
          steps {
             echo ''
          }
        }
      }
    }

  }
}
