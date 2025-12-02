pipeline {
    agent {
        node{
            label 'slave-node'
        }
    }

    environment {
        PATH = "/opt/apache-maven-3.9.11/bin:$PATH"
    }
    stages {
        
         stage('Clone code from GitHub') {
            steps {
                git branch: 'main', url: 'https://github.com/Parthipanrajm/Devops_muliproject'
            }
        }
        
        stage('Build Stage') {
            steps {
                sh 'mvn clean deploy'
            }
        }
        
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
    }
}
