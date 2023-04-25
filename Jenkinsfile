pipeline 
{
    agent any
  
  tools{
    maven "MAVEN_HOME"
  }

    stages 
    {
        stage('Build') 
        {
            steps 
          {
                
                
                echo 'Build App'
                 git  'https://github.com/rcoder23/SpringBoot-Devops.git'
                  bat "mvn -Dmaven.test.failure.ignore=true clean package"
            }
        }

        stage('Test') 
        {
            steps 
            {
                echo 'Test App'
                junit '**/target/surefire-reports/TEST-*.xml'
                archiveArtifacts 'target/*.jar'
            }
        }
      

    }
}
