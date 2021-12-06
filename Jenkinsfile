pipeline
{
    agent any
    stages
    {
        stage('SCM checkout')
        {
            steps{git branch: 'master', url: 'https://github.com/Vishal6747/Ant-WebProject.git'}
        }
        stage('ANT prepare target')
        {
            steps
            {
                withAnt(installation: 'ANT_HOME', jdk: 'JAVA_HOME') {
               sh 'ant prepare'
            }
            }
        }
        stage('ANT init target')
        {
            steps
            {
                withAnt(installation: 'ANT_HOME', jdk: 'JAVA_HOME') {
               sh 'ant init'
            }
            }
        }
    }
}