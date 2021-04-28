pipeline {
    agent any

    stages {
        stage('git') {
            steps {
                git branch: 'main', credentialsId: '60be71a8-fb85-40c3-89d3-e3f41e910d0c', url: 'https://github.com/alonShevach/Test_SAP.git'
            }
        }
        stage('CPU')
        {
            steps {
            sh ''' echo CPU: `top -b -n1 | grep "Cpu(s)" | awk \'{print $2 + $4}\'` 
            FREE_DATA=`free -m | grep Mem` 
            CURRENT=`echo $FREE_DATA | cut -f3 -d\' \'`
            TOTAL=`echo $FREE_DATA | cut -f2 -d\' \'`'''
            }
        }
        stage('Memory')
        {
            steps {
            sh 'echo free -t'
            }
        }
        stage('OS')
        {
            steps {
            sh 'echo cat /proc/version'
            }
        }
    }
}
