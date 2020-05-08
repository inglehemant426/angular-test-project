pipeline {
    agent any
    stages {
        
        stage ('scm checkout') {
            steps {
                git branch: 'master', url: 'https://github.com/inglehemant426/angular-tour-of-heroes/'
            }
        }
        
        stage ('Install Package.json depedancy') {
            steps {
                nodejs('npm') {
                    sh 'node --version'
                    sh 'npm install'
                }
            }
        }
        
        stage ('build') {
            steps {
                nodejs('npm') {
                    sh 'npm run build'
                }
            }
        }
        
    }
}
