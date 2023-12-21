pipeline {
    agent any
    tools {
        maven 'Maven3.9.6'
        jdk 'Java11'
    }
    stages {
        stage ('Build') {
            steps {
                sh 'mvn clean package' 
            }
            post {
                success {
                    junit 'target/surefire-reports/**/*.xml' 
                }
            }
        }
    }
}
