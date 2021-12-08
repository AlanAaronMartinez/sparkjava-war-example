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
                docker run -t --rm --name my-maven-project -v "$(pwd)":/usr/src/mymaven -w /usr/src/mymaven maven:3.3-jdk-8 mvn clean install
                '''
            }
        }
        stage('Deploy') {
            steps {
               sh '''
                docker cp "/root/workspace/Alan_Folder/Alan_Pipeline/target/sparkjava-hello-world-1.0.war" fervent_black:"/usr/local/tomcat/webapps"
                '''
            }
        }
    }
}
