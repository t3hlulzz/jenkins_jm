pipeline
{
    agent any

    stages
    {
        stage ('Build')
        {
        agent { docker { image 'maven:3-alpine' } }
            steps
            {
            sh 'mvn clean install'
            }
        }
        stage ('Test')
        {
        agent { docker { image 'maven:3-alpine' } }
            steps
            {
            sh 'mvn test'
            }
        }
    }
}
