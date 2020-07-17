pipeline {

    agent any
    tools {
        maven 'maven3' 
    }
    stages {
        stage('Compile stage') {
            steps {
                sh "mvn clean compile" 
        }
    }

         stage('testing stage') {
             steps {
                sh "mvn test"
        }
    }

          stage('deployment stage') {
              steps {
                  sshagent(['tomcat.dev']) {
    sh 'scp -o StrictHostKeyChecking=no target/*.war ubuntu@13.127.87.122'
}
                
        }
    }

  }

}
