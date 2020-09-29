pipeline {
  
  agent { label 'kubepods' }

  stages {

    stage('Checkout Source') {
      steps {
        git url:'https://github.com/rahulwagh/jenkins-demo.git'
      }
    }

    stage('Deploy App') {
      steps {
        script {
          kubernetesDeploy(configs: "spring-boot.yml")
        }
      }
    }

  }

}
