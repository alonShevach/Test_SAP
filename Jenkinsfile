pipeline {
    agent any

    stages {
        stage('OS')
        {
            steps {
                sh 'echo uname -a'
                sh 'echo cat /proc/version'
            }
        }
    }
}
