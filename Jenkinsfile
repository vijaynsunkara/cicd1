pipeline {
agent any
stages {
stage('Build Application') {
steps {
bat 'mvn clean install'
}
}
stage('Test') {
steps {
echo 'Application in Testing Phase…'
bat 'mvn test'
}
}
stage('Deploy CloudHub') {
environment {
ANYPOINT_CREDENTIALS = credentials('anypointPlatform')
}
steps {
echo 'Deploying mule project due to the latest code commit…'
echo 'Deploying to the configured environment….'
bat 'mvn package deploy -DmuleDeploy -Dusername="vijaynaidu24" -Dpassword="Sunny123#" -DworkerType=Micro -Dworkers=1'
}
}
}
}
