pipeline {
    agent any
    tools {
        maven 'M2_HOME'
    }

    stages {
        
        stage('build') {
            steps {
                echo 'Hello build'
                sh 'mvn clean'
                sh 'mvn install'
                sh 'mvn package'
                
            }
        }
        stage('deploy') {
            steps {
                build 'deploy_war'
                
            }
        }
        stage('test') {
            steps {
                sh 'mvn test'
                
            }
        }
        
    }
}

