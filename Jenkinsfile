pipeline {
    agent { node { label "AM"}}
    stages {
        stage('primeros pasos') {
            steps {
                sh '''
                echo "hola"
                ls
                pwd
                '''
            }
        }
        stage('Build') {
            steps {
                sh '''
                echo "BUILD"
                '''
            }
        }
        stage('Deploy') {
            steps {
               sh '''
                echo "Deploy"
                '''
            }
        }
    }
}
