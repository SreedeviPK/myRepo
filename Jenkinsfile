  
pipeline {
    agent any 
    tools
    {
        maven 'MAVENHOME'
    }
    stages
    {
        stage('Build')
        {
            steps{
              echo 'Build'
              checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'f93bcc15-102e-45a6-9c99-665d209e10c0', url: 'https://github.com/SreedeviPK/myRepo.git']]])
              sh "mvn -Dmaven.test.failure.ignore=true clean package"
              // git 'https://github.com/SreedeviPK/myRepo.git'
                //sh "mvn clean install"
                //bat "mvn -Dmaven.test.failure.ignore=true clean package"
            }
           /* post{
                success{
                    junit '**target/surefire-reports/TEST-*.xml'
                    archieveArtifacts 'target/*.jar'
                }
            }*/
        } 
    }
  post{
    always{
      junit(
        allowEmptyResults:true,
        testResults: '*test-reports/.xml'
      )
    }
  }
}    


/*pipeline{  
    agent any
    stages{
        stage('SCM Checkout'){
            steps{    
                 git 'https://github.com/SreedeviPK/myRepo'
            }
    }  
    stage('Compile-Package'){
        steps{
         //Get maven home path
         def mvnHome = tool name: 'MAVENHOME', type: 'maven'  
         sh "${mvnHome}/bin/mvn package"
        }
    }
   } 
}*/
