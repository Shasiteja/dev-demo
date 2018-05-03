pipeline {
<<<<<<< HEAD
    agent { label 'Ansible-Master' }
    
    stages {
    	/*stage ('Code Analysis'){
	    steps {
                withSonarQubeEnv('SonarQube') {
			sh 'mvn clean sonar:sonar'
		}
	    }
	}*/

	stage ('Compile Stage'){
	    steps {
	        withMaven(maven : 'Maven'){
		    sh 'mvn clean package'
		}
	    }
	}

	stage ('Deploy to Nexus'){
	    steps {
	        withMaven(maven : 'Maven'){
		    sh 'mvn deploy'
		}
	    }
	}
	stage ('Deploy to QA'){
	    steps {
	            sh 'sudo ansible-playbook /etc/ansible/main.yml'
	    }
	}

=======
    agent any
    stages {
        stage('Checkout') {
            steps {
                echo 'checkout step'
            }
        }
		
        stage('Build') {
            steps {
                
                    echo 'Build step'
                
            }
       	   }
		   
       
	   stage('Deploy'){
	       steps {
		   echo 'deploy step'
	   }
	   }
	   
	   
>>>>>>> ea60a1a7281c0f16eea604ec0c6482be12ca49ed
    }
}
