@Library('mylibrary')_
pipeline
{
    agent any
    stages
    {
        stage('ContDownload_Loan')
        {
            steps
            {
                script
                {
                    cicd.Git("https://github.com/shekharbabu28/maven.git")
                }
            }
        }
        stage('ContBuild_Loan')
        {
            steps
            {
            script
              {
                cicd.Maven()
              }
            }
    
        }
 }
