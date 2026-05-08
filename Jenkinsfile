pipeline {
    agent any

    stages {

        stage('Clone Repository') {
            steps {
                git 'https://github.com/Twinkle-priya/EcommerceApp.git'
            }
        }

        stage('Build') {
            steps {
                bat '"C:\\Program Files\\apache-maven-3.9.15\\bin\\mvn.cmd" clean package'
            }
        }

        stage('Deploy') {
            steps {
                bat 'copy target\\*.war "C:\\Program Files\\Apache Software Foundation\\Tomcat 9.0\\webapps\\"'
            }
        }
    }
}
