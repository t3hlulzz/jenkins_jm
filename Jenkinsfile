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
            sh 'mvn compile war:war -Dversion=${BUILD_NUMBER}'

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
