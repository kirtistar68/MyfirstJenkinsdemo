pipeline {
        agent any
		    stages {
			   stage('Clone repository') {
			   
			    steps {
				checkout scm
				}
			   }
			   stage('Build Image') {
			   steps {
			   sh 'docker build -t myhouseimage -f Dockerfile .'
			   
			   }
			   }
			   stage('Run Image'){
			   steps {
			   sh 'docker run -d --name mycont myhouseimage'
			   }
			   }
			   stage('Testing') {
			   steps {
			   echo 'Testing'
			   }
			   }
			}
}
