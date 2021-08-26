pipeline {
<<<<<<< HEAD

  agent any
  environment {
    //adding a comment for the commit test
    DEPLOY_CREDS = credentials('vijaysun24')
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

=======

  agent any
  environment {
    //adding a comment for the commit test
    DEPLOY_CREDS = credentials('vijaynaidu24')
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

>>>>>>> 84fa158a4a74be2763fcbaa050fe20a61b4f2b27
     stage('Deploy Development') {
      environment {
        ENVIRONMENT = 'Sandbox'
        APP_NAME = 'employee-test-api-dev'
      }
      steps {
            bat 'mvn -U -V -e -B -DskipTests deploy -DmuleDeploy -Dmule.version="%MULE_VERSION%" -Danypoint.username="vijaynaidu24" -Danypoint.password="Sunny123#" -Dcloudhub.app="%APP_NAME%" -Dcloudhub.environment="%ENVIRONMENT%" -Dcloudhub.bg="%BG%" -Dcloudhub.worker="%WORKER%"'
      }
    }
    stage('Deploy Production') {
      environment {
        ENVIRONMENT = 'Production'
        APP_NAME = 'employee-test-api-prod'
      }
      steps {
<<<<<<< HEAD
            bat 'mvn -U -V -e -B -DskipTests deploy -DmuleDeploy -Dmule.version="%MULE_VERSION%" -Danypoint.username="vijaynaidu22" -Danypoint.password="Sunny123#" -Dcloudhub.app="%APP_NAME%" -Dcloudhub.environment="%ENVIRONMENT%" -Dcloudhub.bg="%BG%" -Dcloudhub.worker="%WORKER%"'
=======
            bat 'mvn -U -V -e -B -DskipTests deploy -DmuleDeploy -Dmule.version="%MULE_VERSION%" -Danypoint.username="vijaynaidu24" -Danypoint.password="Sunny123#" -Dcloudhub.app="%APP_NAME%" -Dcloudhub.environment="%ENVIRONMENT%" -Dcloudhub.bg="%BG%" -Dcloudhub.worker="%WORKER%"'
>>>>>>> 84fa158a4a74be2763fcbaa050fe20a61b4f2b27
      }
    }
  }

  tools {
    maven 'M3'
  }
<<<<<<< HEAD
}
=======
}
>>>>>>> 84fa158a4a74be2763fcbaa050fe20a61b4f2b27
