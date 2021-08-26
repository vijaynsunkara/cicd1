pipeline {
   agent any
  environment {
    //adding a comment for the commit test
    DEPLOY_CREDS = credentials('anypointPlatform')
    MULE_VERSION = '4.3.0'
    BG = "vijay sun"
    WORKER = "Micro"
  }
  stages {
    stage('Build') {
      steps {
            bat 'mvn -B -U -e -V clean -DskipTests package'
      }
    }

    stage('Test') {
      steps {
          bat "mvn test"
      }
    }


     stage('Deploy Development') {
      environment {
        ENVIRONMENT = 'Sandbox'
        APP_NAME = 'employee-test-api-dev'
      }
      steps {
            bat 'mvn -U -V -e -B -DskipTests deploy -DmuleDeploy -Dmule.version="4.3.0" -Danypoint.username="vijaynaidu24" -Danypoint.password="Sunny123#" -Dcloudhub.app="employee-test-dev" -Dcloudhub.environment="Sandbox" -Dcloudhub.bg="vijay sun" -Dcloudhub.worker="1"'
      }
    }
    stage('Deploy Production') {
      environment {
        ENVIRONMENT = 'Production'
        APP_NAME = 'employee-test-api-prod'
      }
      steps {

            bat 'mvn -U -V -e -B -DskipTests deploy -DmuleDeploy -Dmule.version="4.3.0" -Danypoint.username="vijaynaidu22" -Danypoint.password="Sunny123#" -Dcloudhub.app="employee-test-prod" -Dcloudhub.environment="Sandbox" -Dcloudhub.bg="vijay sun" -Dcloudhub.worker="1"'

            

      }
    }
  }

  tools {
    maven 'M3'
  }

}


