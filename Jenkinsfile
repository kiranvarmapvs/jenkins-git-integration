pipeline {
	agent any
	stages {
		stage ('Git-Checkout')
		{
			steps
			{
			    echo "Accessing bat files from github repo"
			    git 'https://github.com/amitvermaa93/jenkins-git-integration.git'
			}
		}
		stage ('MAVEN-VALIDATE')
		{
		  steps
		  {
		      echo "Validating maven repository"
		      bat 'mvn validate'
		  }
		}
		stage ('MVAEN-COMPILE')
		{
		  steps
		  {
		      echo "Compiling maven project"
		      bat 'mvn compile'
		  }
		}
		stage ('MAVEN-PACKAGING')
		{
		  steps
		  {
		      echo "Packaging to war file"
		      bat 'mvn package'
		  }
		}
		stage ('MAVEN-INSTALL')
		{
		  steps
		  {
		      echo "INSTALLING TO LOCAL .M2 REPOSITORY"
		      bat 'mvn install'
		  }
		}
	}
}
