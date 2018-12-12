pipeline {
 agent any
stages {
 stage('CodeCheckout') {
 steps {
 script {
    checkout scm
     def mvnHome = tool 'maven-3'
     def javaHome = tool 'JAVA_1.8'
     }
    }
   }
   
 stage('build customer app code') { 
 steps {
  script {
        def mvnHome = tool 'maven-3'
        def javaHome = tool 'JAVA_1.8'
        sh 'mvn clean install'
    }
  }
 }
 stage('Testing'){
						stage ('Functional Testing'){
					steps {
						script {
							echo "Functional Testing"
							}
					}
				}}
    
     stage('Consumer'){
		
				stage ('User Acceptance Testing'){
					steps {
						script {
							echo "User Acceptance Testing"
							}
					}
				}}
}
}
