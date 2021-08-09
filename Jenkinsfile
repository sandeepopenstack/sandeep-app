// Added for demo
node{
   stage('SCM Checkout'){
     git 'https://github.com/sandeepopenstack/sandeep-app.git'
   }
   stage('Compile-Package'){
      // Get maven home path
      def mvnHome =  tool name: 'maven-3', type: 'maven'
      sh "${mvnHome}/bin/mvn package"
   }


   stage('Email Notification'){
      mail bcc: '', body: '''Hi Welcome to jenkins email alerts
      Thanks
      Hari''', cc: '', from: '', replyTo: '', subject: 'Jenkins Job', to: 'sandeeplinux1068@gmail.com'
   }

}
