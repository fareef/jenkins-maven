pipeline {
    agent any 
    stages {
        stage('git Clone') { 
            steps {
                sh "git clone https://github.com/fareef/jenkins-maven.git" 
                sh "mvn clean -f jenkins-maven"
                // 
            }
        }
        stage('Test') { 
            steps {
                sh "mvn test -f jenkins-maven"
                // 
            }
        }
        stage('Deploy') { 
            steps {
                sh "mvn package -f jenkins-maven"
                // 
            }
        }
    }
}
