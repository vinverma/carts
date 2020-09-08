pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'compiling and Building..'
        sh 'mvn clean compile'
      }
    }

    stage('test') {
      steps {
        echo 'Running Test cases'
        sh 'mvn test'
      }
    }

    stage('package') {
      steps {
        echo 'Packaging....'
        sh 'mvn install -DskipTests'
      }
    }

  }
  tools {
    maven 'Maven 3.6.3'
  }
}