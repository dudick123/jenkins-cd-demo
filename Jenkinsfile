pipeline {
  agent any
  stages {
    stage('Pre-Build') {
      agent any
      steps {
        echo 'Step 1'
        echo 'Step 2'
        echo 'Step 3'
        echo 'Step 4'
      }
    }
    stage('Build') {
      parallel {
        stage('Web Deployment') {
          steps {
            echo 'Prepare Web Image'
          }
        }
        stage('Database Deployment') {
          steps {
            echo 'Prepare DDL Image'
            echo 'Prepare DML Image'
          }
        }
      }
    }
    stage('Run') {
      steps {
        echo 'Run Database Server Container'
        echo 'Run DDL Container'
        echo 'Run DML Container'
        echo 'Run Web Container'
      }
    }
    stage('Validate') {
      parallel {
        stage('Web Validation') {
          steps {
            echo 'Test Web Container'
          }
        }
        stage('Database Validation') {
          steps {
            echo 'Run DDL Validation'
            echo 'Run DML Validation'
          }
        }
      }
    }
  }
}