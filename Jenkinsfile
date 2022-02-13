pipeline {
    agent { docker 'maven:3.5-alpine'}
    stages ('First step') {
       steps {
          git 'https://github.com/SerhiyEnergo/spring-petclinic.git'
       }
    }
    stages ('Build) {
        steps {
            sh 'mvn clean package'
            junit '**/target/surefire-reports/TEST-*.xml
        }
    }
  }
 }
  
