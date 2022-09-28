pipeline
{
    agent any
    tools
    {
        maven "Maven"
    }
    
    triggers 
    {
      pollSCM '* * * * *'
    }

    stages
    {
        //Checkout From Git
        stage('Checkout SCM')
        {
            steps
            {
              git branch: 'master', credentialsId: '034672a4-2c42-46e2-956c-12b44d44a50e', url: 'https://github.com/Home-Practice/MVC-Thymeleaf-App.git'

            }
        }

        //Maven Build
        stage('Maven Build')
        {
            steps
            {
                sh "mvn clean package"
            }
        }
    }
}
