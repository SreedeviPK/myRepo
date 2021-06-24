pipeline{  
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
}
