pipeline {
    agent {
	node {
	    label "any"
	}
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -DskipTests clean package' 
            }
        }
        stage('Test') { 
            steps {
                sh 'mvn test' 
            }
        }
    }
}
