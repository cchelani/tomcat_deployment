#!/usr/bin/env groovy

pipeline {

    agent {
        docker {
            image 'centos'
            args '-u root'
        }
    }

    stages {
        stage('Install') {
            steps {
                echo 'installing tomcat packages...'
                sh 'yum install -y tomcat'
            }
        }
        stage('Starting Service') {
            steps {
                echo 'Starting tomcat services...'
                sh '/usr/sbin/tomcat start'
            }
        }
    }
}
