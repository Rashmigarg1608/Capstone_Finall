pipeline{
    agent any
    environment { 
        registry = "rashmigarg16/application" 
        registryCredential = 'rashmi' 
        dockerImage = '' 
    }    
    tools { 
        maven 'Maven 3.8.5' 
    }
    stages
       {
          stage("Build")
            {
                steps{
                    sh "mvn compile"
                }
                
            }
            stage("Test")
            {
                steps{
                    sh "mvn clean test"
                }
            }
            stage("Package")
            {
                steps{
                    sh "mvn clean package"
                }
            }
      }
}
