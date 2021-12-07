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
                mvn clean install
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
