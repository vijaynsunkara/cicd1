pipeline
{
agent any
stages{
	stage('Build application')
	{
	steps{
	bat 'mvn clean install -DskipMunitTests'
	}
	}
	stage('Deploy application to cloud hub')
	{
	steps
	{
	bat 'mvn package deploy -DmuleDeploy'
	}
	}
}

}