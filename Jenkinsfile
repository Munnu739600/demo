pipeline {
  agent any
  stages {
    stage('Unit') {
      steps {
       bat 'mvn clean test'
      }
    }    
    stage('Deploy CloudHub') {
      steps {
        bat 'mvn deploy -DmuleDeploy -Dcloud.env=Sandbox -Danypoint.businessGroup=<BusinessGroup> -Dcloudhub.workerType=Small -DcloudhubAppName=ramlapikitmule4 -Dmule.version=4.1.5 -Dcloud.user=<cloudUser> -Dcloud.password=****'
      }
    }
  }
}
