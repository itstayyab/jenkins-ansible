pipeline {
    agent any
    stages {
        stage("Stage 1") {
            when { branch 'master' }
            steps{
                echo 'Found master'
            }
        }
         stage("master") {
             when { branch 'integration' }
                steps{
                echo 'Found integration'
            }
         
        }
    }
}