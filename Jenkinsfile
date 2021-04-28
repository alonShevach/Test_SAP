pipeline {
    agent any

    stages {
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
                sh 'echo cat /etc/*release'
                sh 'echo cat /proc/version'
            }
        }
    }
}
