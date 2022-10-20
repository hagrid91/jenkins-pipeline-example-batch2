pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''echo \'this is for build\'
pwd
date'''
      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            echo 'this is for test'
          }
        }

        stage('') {
          steps {
            echo 'this for testing 2'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        echo 'this for deploy'
      }
    }

  }
}