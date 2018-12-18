node{
   stage('SCM Checkout'){
     git 'https://github.com/pnewalkar/my-application'
   }
   stage('Compile-Package'){
      def mvnHome =  tool name: 'maven_3_5_0', type: 'maven'   
      sh "${mvnHome}/bin/mvn package"
   }
   stage('Testing Stage'){
      def mvnHome =  tool name: 'maven_3_5_0', type: 'maven'   
      sh "${mvnHome}/bin/mvn test"
   }
}
