#!groovy
node('slave1') {
   // Mark the code checkout 'stage'....
   stage ('Checkout'){
      // Get some code from a GitHub repository
      checkout scm
   }

   // Mark the code build 'stage'....
   stage ('Build Gradle'){
      // Get the maven tool.
      // ** NOTE: This 'maven3' maven tool must be configured
      // **       in the global configuration.
      def gradleHome = tool 'gradle4'
      // Run the maven build
      //sh "${gradleHome}/bin/gradle build"
      sh "${gradle4}/bin/gradle clean jar"
   }
}
