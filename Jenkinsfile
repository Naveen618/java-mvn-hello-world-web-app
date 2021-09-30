pipeline {
  agent {label 'slave2'}
  stages {
   
stage ('build'){
      steps{
        sh 'pwd'
        sh 'ls'
        sh 'docker build -t mstage:latest .'
      }
    }
   
     stage ('publish'){
      steps{
        sh 'docker tag mstage:latest naveen618/mstagedh:1.0'
        sh 'docker login -u naveen618 -p Naveen1518'
        sh 'docker push naveen618/mstagedh:1.0'
      }
    }
   
  stage ('deploy'){
    agent {label 'slave2'}
      steps{
        sh 'docker login -u naveen618 -p Naveen1518'
        sh 'docker pull naveen618/mstagedh:1.0'
        sh 'docker run -d -p 9000:8080 naveen618/mstagedh:1.0'
      }
  }
  }
}
