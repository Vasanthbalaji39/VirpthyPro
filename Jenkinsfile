pipeline {
     agent any
stages {
    stage('Source Code Checkout') { // for display purposes..
        echo 'source code is checkout out'
        git credentialsId: 'Github-ID', url: 'https://github.com/DKPMOrg/VirpthyPro.git'
        }
   stage('Build and Test') {
     echo 'Build is triggered with test execution'
       steps{ 
            withMaven(maven : 'Maven-3.5.2'){
            sh 'mvn clean compile'
            }
         }
     } 
   
   stage('Deploy to DEV') {
     echo 'Deploying to Dev environment'
     }
   stage('Test Execution on Dev') {
     echo 'Test execution on Dev'
     //sh 'mvn test'
   }
 }
}
