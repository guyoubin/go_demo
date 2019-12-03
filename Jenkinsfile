pipeline {
   agent any
   stages {
      stage('Poll SCM') {
         steps {
            git url: 'https://github.com/guyoubin/go_demo.git'
         }
      }
      stage('Static Code Analysis') {
         steps {
            sh 'sonar-scanner -Dsonar.host.url=http://192.168.195.138:9000 -Dsonar.projectKey=go_demo -Dsonar.projectName=go_demo -Dsonar.sources=. -Dsonar.sourceEncoding=UTF-8 -Dsonar.language=go '
         }
      }
   }
}
