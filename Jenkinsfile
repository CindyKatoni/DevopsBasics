pipeline {
    tools {
        jdk 'myjava'
        maven 'mymaven'
    }
    agent any
    stages {
        stage('Checkout') {
            steps {
                echo 'Cloning...'
                git 'https://github.com/CindyKatoni/DevopsBasics.git'
            }
        }
        stage('Compile') {
            steps {
                echo 'Compiling...'
                sh 'mvn compile'
            }
        }
        stage('Code Review') {
            steps {
                echo 'Performing Code Review...'
                sh 'mvn pmd:pmd'
            }
        }
        stage('Package') {
            steps {
                echo 'Packaging...'
                sh 'mvn package'
            }
        }
    }
}
