Jenkinsfile
    pipeline {
        agent any

        stages {
            stage('Pull Source Code') {
                steps {
                    git branch: 'main', url: 'https://github.com/jatisatrio1/e-voting-app.git'
                }
            }
            stage('Build Container') {
                steps {
                    sh 'docker compose build'
                }
            }
            stage('Deploy Container Apps') {
                steps {
                    sh 'docker compose up -d'
                }
            }
            stage('Push Image') {
                steps {
                    sh 'docker compose push'
                }
            }
        }
    }
