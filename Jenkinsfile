#!/usr/bin/env groovy

pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo 'in Build stage ---->'
            }
        }
        stage('Test') {
            steps {
                 echo 'in test stage ---->'
            }
        }
    }
    post {
        always {
            echo 'One way or another, I have finished'
            deleteDir() /* clean up our workspace */
        }
        success {
            echo 'I succeeeded!'
        }
        unstable {
            echo 'I am unstable :/'
        }
        failure {
            echo 'I failed :('
        }
        changed {
            echo 'Things were different before...'
        }
    }
}
