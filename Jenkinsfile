pipeline {
  agent { label 'master' }

  tools {
    jdk 'Java'
    maven 'Maven'
  }
  
  environment {

      sonar_url = 'http://172.31.93.142:9000'
      sonar_username = 'admin'
      sonar_password = 'admin'
      nexus_url = '172.31.93.142:8081'
      artifact_version = '4.0.0'

 } 

stages {
    stage('Git checkout'){
      steps {
        git branch: 'develop',
        url: 'https://github.com/chinni4321/helloworld.git'
      }
    }
    stage('Maven build'){
      steps {
        sh 'mvn clean install'
      }
    }
}
}
