pipeline{
    agent any
    environment { 
        registry = "rashmigarg16/application" 
        registryCredential = 'rashmi' 
        dockerImage = '' 
    }    
    tools { 
        maven 'maven 3.8.4' 
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
