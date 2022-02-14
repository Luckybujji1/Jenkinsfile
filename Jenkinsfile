pipeline {
    agent any

    stages {
        stage('continuos down') {
            steps {
                git 'https://github.com/Luckybujji1/DemoATC.git'
            }
        }
         stage('continuos build') {
             steps {
                 sh 'mvn install'
            }
        }
         stage('continuos deploy') {
             steps {
                 sh 'sshpass -p "laxmi" scp target/DemoATR.war laxmi@172.17.0.2:/opt/apache-tomcat-9.0.58/webapps'
            }
        }
    }
}

