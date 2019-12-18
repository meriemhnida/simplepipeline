pipeline {
    agent any
    tools {
          maven 'MAVEN 3'
     jdk 'jdk1.8.0_172'
    }
    stages {
        
        stage ('Build') {
            steps {
            bat 'mvn install'
            }
            post {
                success {
                    junit 'target/surefire-reports/**/*.xml' 
                }
            }
        }
    }
}
