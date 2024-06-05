@Library('shared-library')_
pipeline {
    agent {
        label 'default'
        
    }
    stages{
        stage (DockerBuild){
            steps{
                                 buildDockerImage("tryimg")  
            }
        }
    }
    
}
