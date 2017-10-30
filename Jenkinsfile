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
            sh 'echo $USER'
            //sh 'mvn clean install'
            }
        }
        stage ('archive artifacts')
        {
        steps
        {
        archiveArtifacts artifacts: '*.jar', onlyIfSuccessful: true
        }
        }
    }
}
