node{  
    stage('SCM Checkout'){
        git 'https://github.com/SreedeviPK/myRepo'
    }  
    stage('Compile-Package'){
      //Get maven home path
      def mvnHome = tool name: 'MAVENHOME', type: 'maven'  
      sh "${mvnHome}/bin/mvn package"
    }
 
}
