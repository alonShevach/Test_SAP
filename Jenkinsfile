pipeline {
    agent any

    stages {
        stage('CPU')
        {
            steps {
                sh 'cat /proc/cpuinfo'
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
