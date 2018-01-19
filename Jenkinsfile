pipeline {
  agent any
    triggers {
        cron('H */4 * * 1-5')
  }
  stages {
    stage('Stage 1') {
      agent any
      steps {
        echo 'Step 1'
        echo 'Step 2'
        echo 'Step 3'
        echo 'Step 4'
      }
    }
    stage('Stage 2-BP') {
      steps {
        echo 'Step 1'
        echo 'Step 2'
      }
    }
  }
}
