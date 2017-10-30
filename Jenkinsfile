pipeline
{
    agent any
//
    stages
    {
    agent { docker { image 'maven:3-alpine' } }
        stage ('build')
        {
            steps
            {
            sh 'mvn clean install'
            }
        }
    }
}
