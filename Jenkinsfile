pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'this is build the app job'
        sh 'mvn compile'
      }
    }

    stage('test') {
      steps {
        echo 'this is test the app job'
        sh 'mvn test'
      }
    }

    stage('package') {
      steps {
        echo 'this is package the app job'
        sh 'mvn package'
      }
    }

    stage('archive') {
      steps {
        archiveArtifacts '**/target/*.jar'
      }
    }

  }
  tools {
    maven 'maven'
  }
  post {
    always {
      echo 'This pipeline has completed...'
    }

  }
}