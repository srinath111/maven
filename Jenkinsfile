@Library('srilibrary')_
pipeline
{
    agent any
    stages
    {
        stage('continuous Download')
        {
            steps
            {
              script
                {
                  cicd.newGit("https://github.com/srinath111/maven.git")
                }
            }
        }
        stage('continuous Built')
         {
             steps
             {
                 script
                 {
                     cicd.newmaven()
                 }
             }
         }
         stage('continuous Deployment')
         {
             steps
             {
                 script
                 {
                     cicd.newDeploy()
                 }
             }
         }
        
        stage('continuous Testing')
        {
            steps
            {
              script
                {
                  cicd.newGit("https://github.com/intelliqittrainings/FunctionalTesting.git")
                  cicd.newTest()
                  
                }
            }
        }
         stage('continuous delivery')
         {
             steps
             {
                 script
                 {
                     cicd.newDel()
                 }
             }
         }
    }
}
