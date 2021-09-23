pipeline {
   agent any
   stages {
  
 
   stage('checkout') {
         
        	steps {
               sh 'rm -rf *'
         		sh 'git clone https://github.com/Naveen618/java-mvn-hello-world-web-app'
  
          }
    
    }
 
stage('build') {
         
        	steps {
            cd /home/slave2/workspace/Pipelinejob/java-mvn-hello-world-web-app
            sh 'pwd'
            sh 'ls'
 sh 'mvn package'
}
}

   }

}
