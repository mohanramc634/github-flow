pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'chmod +x test.sh'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh './test.sh'
            }
        }
        stage('Deploy') {
            when {
                branch 'main'
            }  
            steps {
                echo 'Deploying....'
            }
        }
    }
}
