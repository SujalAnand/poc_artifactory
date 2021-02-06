pipeline {
    agent any
	
	    environment {
		            USER_CREDENTIALS = credentials('AnypointExchangeID')
					NEXUS_CREDENTIALS = credentials('nexus')
					USER_KEY = credentials('key')        
    }

    stages {
		stage('Build Application') {
            steps {
                echo "----Building the Application------ "
                bat 'mvn clean package'
            }
        }
        stage('Deploy Application') {
            steps {
                echo "----Deploying To MuleSoft------ "
               // bat 'mvn package deploy -nsu -DskipMunitTests -DmuleDeploy -Danypoint.username=%USER_CREDENTIALS_USR% -Danypoint.password=%USER_CREDENTIALS_PSW% -Denv=dev -Dkey=%USER_KEY%'
            }
        }


    }
}
