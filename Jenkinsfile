#!/usr/bin/env groovy

pipeline {

    agent {
        docker {
            image 'node:alpine'
            args '-p 3000:3000'
        }
    }
  
    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                sh 'npm test'
            }
        }
        stage('Deploy') {
            steps {
               echo 'Deploying...'
               sh 'npm start'
            }
        }    
    }
}
