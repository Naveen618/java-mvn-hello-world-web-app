pipeline {
agent {label: 'slave2'}
   stages {
  
 
   stage('checkout') {
         
        	steps {
      
         		sh 'git clone https://github.com/Naveen618/java-mvn-hello-world-web-app'
  
          }
    
    }
 
stage('build') {
         
        	steps {
  
 sh 'mvn package'
}
}

   }

}
