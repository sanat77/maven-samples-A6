pipeline {
  agent any
  tools { 
      maven 'DHT_MVN' 
      jdk 'DHT_SENSE' 
  }
  stages {
    stage('check out') {
      steps {
        git(url: 'https://github.com/sanat77/maven-samples-A6', branch: 'master')
      }
    }
    stage('run') {
      steps {
        sh 'mvn verify'
      }
    }
  }
}
