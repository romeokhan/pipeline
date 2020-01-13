pipeline {
  agent any
  stages {
    stage ( 'checkout') {
      steps {
   checkout scm
      }
   }
   stage ('compile stage') {
   steps {
   withMaven(maven  : 'maven-3.6.3') {
   sh 'mvn clean compile'
   }
 }
}

stage ('Deploy') {
   steps {
   withMaven(maven  : 'maven-3.6.3') {
   sh 'mvn deploy'
   }
 }
}
}
}

   
