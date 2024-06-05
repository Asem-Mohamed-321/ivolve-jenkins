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

        stage(Dockerpush){
            steps{
                                pushDockerImage("tryimg")
            }
        }

        stage(OpenshiftDeployment){
            steps{
                                openshiftDeployment()
            }
        }
    }
    
}
