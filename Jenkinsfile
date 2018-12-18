node{
   stage('SCM Checkout'){
     git 'https://github.com/pnewalkar/my-application'
   }
   stage('Compile-Package'){
      def mvnHome =  tool name: 'maven_3_5_0', type: 'maven'   
      sh "${mvnHome}/bin/mvn package"
   }
      stage('Deploy'){
      def mvnHome =  tool name: 'maven_3_5_0', type: 'maven'   
      sh "${mvnHome}/bin/mvn deploy:deploy-file -DgeneratePom=false -DrepositoryId=nexus -DrepositoryId=nexus -Durl=http://35.231.153.198:8081/nexus/content/repositories/releases -DpomFile=pom.xml -Dfile=target/myweb-0.0.5.war"
         }
}
