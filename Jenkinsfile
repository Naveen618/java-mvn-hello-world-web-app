pipeline {
   agent any
    stages {
        stage('Directory') {
            steps {
               // sh 'cd /home/slave2/workspace/Pipelinejob/java-mvn-hello-world-web-app/'
               sh 'cd ${WORKSPACE}'
            }
        }
        stage('Compile') {
            steps {
                sh 'mvn compile'
            }
        }
        stage('Package') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
