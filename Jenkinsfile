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
                docker cp "/root/workspace/Pipeline_AlanMartinez/target/sparkjava-hello-world-1.0.war" tomcat:"/usr/local/tomcat/webapps"
                '''
            }
        }
    }
}
