#!groovy
pipeline 
{
    agent any

    stages 
    {
        stage('SCM') 
        {
            environment
            {
                GLOB_MEC_ENV              = 'DEV'
                GLOB_MEC_GITAPP           = 'markbullock4/python-web-repository'
            }
            steps 
            {
                //get app
                echo "Jenkins Environment is : ${env.GLOB_MEC_ENV}"
                git url: "https://github.com/${env.GLOB_MEC_GITAPP}"
            }
        }
        
        stage('Build')
        {
             steps
             {
                echo "Jenkins Build stage"
             }
        }

        stage('Test')
        {
             steps
             {
                echo "Jenkins Test stage"
             }
        }

        stage('Tidy')
        {
             steps
             {
                echo "Jenkins Tidy stage"
             }
        }
    }
}        
