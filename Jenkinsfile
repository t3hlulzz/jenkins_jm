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
            sh 'mvn clean install -Dversion=${BUILD_NUMBER}'
            }
        }
        stage ('Test')
        {
        agent { docker { image 'maven:3-alpine' } }
            steps
            {
            sh 'mvn test'
            archiveArtifacts '**/target/*.jar'
            }
        }
    }
    //post
    //{
    //  success
    //  {
    //   archiveArtifacts '**/target/*.jar'
    //  }
    //}
}
