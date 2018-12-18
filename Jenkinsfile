node{
   stage('SCM Checkout'){
     git 'https://github.com/pnewalkar/my-application'
   }
   stage('Compile-Package'){
      // Get maven home path
      def mvnHome =  tool name: 'maven_3_5_0', type: 'maven'   
      sh "${mvnHome}/bin/mvn package"
   }
}
