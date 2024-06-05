@Library('shared-library')_
pipeline {
    agent {
        label 'slave'
        
    }
    stages{
        stage (DockerBuild){
        steps{
                                 buildDockerImage("ivolveimg")  
            }
        }

        stage(Dockerpush){
            steps{
                                pushDockerImage("ivolveimg")
            }
        }

        stage(OpenshiftDeployment){
            steps{
                                openshiftDeployment()
            }
        }
    }
    
}
