pipeline {
    agent any

    stages {
        stage('CPU')
        {
            steps {
                sh 'cat /proc/cpuinfo | grep processor | wc -l '
            }
        }
        stage('Memory')
        {
            steps {
            sh 'free -t'
            }
        }
        stage('OS')
        {
            steps {
                sh 'cat /etc/os-release'
            }
        }
    }
}
