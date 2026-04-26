pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'YOUR_GITHUB_REPO_LINK'
            }
        }

        stage('Run Python Script') {
            steps {
                bat 'python analyzer.py'
            }
        }

        stage('Archive Report') {
            steps {
                archiveArtifacts artifacts: 'report.txt', fingerprint: true
            }
        }
    }
}