pipeline {
    agent any
    stages {
        stage("Stage 1") {
            when { branch 'master' }
            steps{
                sh 'ansible-playbook site.yml'
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