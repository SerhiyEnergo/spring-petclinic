pipeline {
    agent { docker 'maven:3.6-alpine' }
    stages {
        stage ('Checkout') {
          steps {
            git branch: 'main', credentialsId: 'petclinic_jenkis_git', url: 'git@github.com:SerhiyEnergo/spring-petclinic.git'
            sh 'pwd'
            sh 'ls -la'
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
