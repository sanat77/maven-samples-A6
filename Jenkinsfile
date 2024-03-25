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
        // sh 'git bisect start 8bad1c6db9cf6930abd8e52ff5dfdd046194ae9b 98ac319c0cff47b4d39a1a7b61b4e195cfa231e5'
        // sh 'git bisect run mvn clean test'
        // sh 'mvn clean test'
        sh 'echo "Testing"'
      }
    }

  }
}
