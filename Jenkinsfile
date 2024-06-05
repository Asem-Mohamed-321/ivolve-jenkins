@Library('shared-library')_
pipeline {
    agent {
        label 'slave'
        
    }
    stages{
        stage (DockerBuild){
        steps{
                                 buildDockerImage("iVolveimg")  
            }
        }

        stage(Dockerpush){
            steps{
                                pushDockerImage("iVolveimg")
            }
        }

        stage(OpenshiftDeployment){
            steps{
                                openshiftDeployment()
            }
        }
    }
    
}
