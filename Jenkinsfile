pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "MAVEN_HOME"
    }

    stages {
        
        stage('Git clone'){
            steps{
                 git 'https://github.com/jglick/simple-maven-project-with-tests.git'
            }
        }
        
        stage('Build') {
            steps {
                bat "mvn -Dmaven.test.failure.ignore=true clean package"
                
            }
        }
        
        
        
         stage('Test') {
            steps {
               bat "mvn test"
            }
         }
         
        
        
    }
}
