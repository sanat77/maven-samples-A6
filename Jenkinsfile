pipeline {
  agent any
  tools { 
      maven 'DHT_MVN' 
      jdk 'DHT_SENSE' 
  }
  stages {
    stage('check out') {
      steps {
        git(url: 'https://github.com/dhetong/maven-samples-A6.git', branch: 'master')
      }
    }

    stage('run') {
      steps {
        sh 'git bisect start 8bad1c6db9cf6930abd8e52ff5dfdd046194ae9b 98ac319c0cff47b4d39a1a7b61b4e195cfa231e5'
        sh 'git bisect run mvn clean test'
        sh 'git checkout 34d31973a0cc1f3d77cd5038fc9c01eeba7ec183'
        sh 'mvn clean test'
      }
    }

  }
}
