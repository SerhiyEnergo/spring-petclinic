pipeline {
    agent { docker 'maven:3.6.3-alpine'}
    stages {
        stage ('Checkout') {
          steps {
            git 'https://github.com/SerhiyEnergo/spring-petclinic.git'
          }
        }
        stage ('Build') {
            steps {
                sh 'mvn clean package'
                junit '**/target/surefire-reports/TEST-*.xml'
            }
        }
    }
}
