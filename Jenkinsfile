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
        stage ('archive artifacts')
        {
        archiveArtifacts artifacts: '*.jar', onlyIfSuccessful: true
        }
    }
}
