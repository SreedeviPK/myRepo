node{
  stages{
    stage('SCM Checkout'){
        git 'https://github.com/SreedeviPK/myRepo'
    }  
    stage('Compile-Package'){
    sh 'mvn package'
    }
  }
}
