@Library('mylibrary')_
pipeline
{
    agent any
    stages
    {
        stage('ContDownload_master')
        {
            steps
            {
                script
                {
                    cicd.Git("https://github.com/shekharbabu28/maven.git")
                }
            }
        }
        stage('ContBuild_master')
        {
            steps
            {
            script
              {
                cicd.Maven()
              }
            }
    
        }
        stage('ContDeployment_master')
        {
            steps
            {
                script
                {
                    cicd.Deploy("DeclarativePipelineWithSharedLibraries","172.31.31.174", "testingapp")
                }
            }
        }
        stage('ContTesting_master')
        {
            steps
            {
                script
                {
                    cicd.Git("https://github.com/intelliqittrainings/FunctionalTesting.git")
                    cicd.Testing("DeclarativePipelineWithSharedLibraries")
                }
            }
        }
        stage('ContDelivery_master')
        {
            steps
            {
                script
                {
                    cicd.Deploy("DeclarativePipelineWithSharedLibraries","172.31.23.99", "prodapp")
                }
            }
        }
    }
    
}
