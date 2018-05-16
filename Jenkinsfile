pipeline {
    agent any
    stages {
        stage("Stage 1") {
            when { branch 'master' }
            steps{
                sh 'docker run -d --rm -p 8888:8080 jenkins-ansible'
            }
        }
         stage("master") {
             when { branch 'integration' }
                steps{
                sh 'docker build  -t jenkins-ansible .'
            }
         
        }
    }
}