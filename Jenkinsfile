pipeline {

  agent any 
  stages {
     stage('clean workspace') {
      steps {
        // Clean before build
                cleanWs()
                // We need to explicitly checkout from SCM here
                checkout scm
                echo "Building ${env.JOB_NAME}..." 
 }
 }
 
 stage('Code Checkout') {
  steps {
checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: '956db50b-297d-4797-b42f-dce67ea6a917', url: 'https://github.com/Tejindrakhatri/CICD.git']]])
  }
  }
 }
}
