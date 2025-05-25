pipeline {
    agent {
      kubernetes {
        cloud 'openshift'
        yamlFile 'jenkins-agent-maven.yaml'
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
