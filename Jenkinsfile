pipeline {
     agent any
stages {
    stage('Source Code Checkout') { // for display purposes..
         steps{ 
               echo 'source code is checkout out'
               git credentialsId: 'Github-ID', url: 'https://github.com/DKPMOrg/VirpthyPro.git'
               }
      }
   stage('Build and Test') {
         steps{ 
             //withMaven requires Pipeline maven integration plugin.
            withMaven(maven : 'Maven-3.5.2'){
            echo 'Build is triggered with test execution'
            sh 'mvn clean compile'
            }
         }
     } 
   
   stage('Deploy to DEV') {
        steps{   
               echo 'Deploying to Dev environment'
             }
   }
   stage('Test Execution on Dev') {
        steps{
               echo 'Test execution on Dev'
     //sh 'mvn test'
             }
   }
 }
}
