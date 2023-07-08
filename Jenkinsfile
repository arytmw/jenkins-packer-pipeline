pipeline {
  agent any

  stages {
    stage('Packer - Validate image') {
      steps {
        sh """
        packer validate tomcat8_ojdk8.json 
        """
      }
    }
    stage('Packer - Build Image') {
      steps {
        sh """
        packer build tomcat8_ojdk8.json
        """
      }
    }
  }
}
