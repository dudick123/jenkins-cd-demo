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
            echo 'Build Docker Image'
          }
        }
        stage('Database Deployment') {
          steps {
            echo 'Perform Database Updates'
            echo 'Database DDL Updates'
            echo 'Database DML Updates'
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
            echo 'Test Docker Containers'
          }
        }
        stage('Database Validation') {
          steps {
            echo 'DDL Validation'
            echo 'DML Validation'
          }
        }
      }
    }
  }
}