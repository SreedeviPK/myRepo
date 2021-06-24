  
pipeline {
    agent any 
    tools
    {
        maven "MAVENHOME"
    }
    stages
    {
        stage('Build')
        {
            steps{echo 'Build'
                //git 'https://github.com/SreedeviPK/myRepo.git'
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
   } */
}
