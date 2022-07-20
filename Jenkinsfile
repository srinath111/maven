@Library('srilibrary')_
pipeline
{
    agent any
    stages
    {
        stage('continuous Download_Loans')
        {
            steps
            {
              script
                {
                  cicd.newGit("https://github.com/srinath111/maven.git")
                }
            }
        }
        stage('continuous Built_Loans')
         {
             steps
             {
                 script
                 {
                     cicd.newmaven()
                 }
             }
         }
}
