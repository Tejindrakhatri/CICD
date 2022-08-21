pipeline {
  node{
      label 'slave01'
}
  agent any 
  stages {
     stage('clean workspace') {
      steps {
       
         sh """
           echo "clean the workspace for $APP_NAME"
           echo "we are in stage 1"
           """    
 }
 }
 
 stage('Code Checkout') {
  steps {
checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: '956db50b-297d-4797-b42f-dce67ea6a917', url: 'https://github.com/Tejindrakhatri/CICD.git']]])
  }
  }
 }
}
