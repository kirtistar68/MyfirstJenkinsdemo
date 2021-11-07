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
			   sh 'docker build -t myhouseimage -p 5000:4000 -f Dockerfile .'
			   
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
