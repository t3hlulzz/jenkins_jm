pipeline
{
    agent any

    stages
    {
        stage ('build')
        {
        agent { docker { image 'maven:3-alpine' } }
            steps
            {
            sh 'mvn clean install'
            }
        }
        stage ('test')
        {
        agent { docker { image 'maven:3-alpine' } }
            steps
            {
            sh 'mvn test'
            }
        }
    }
}
