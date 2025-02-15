pipeline {
    agent any
    stages{
        stage('Build') {
            steps{
            sh 'sudo apt update'
            sh 'sudo apt install apache2 -y'
            }
        }
        stage('Results') {
            steps{
                sh 'sudo systemctl start apache2'
                sh 'sudo systemctl status apache2'
                echo 'Apache is corrected install'
                sh 'sudo cat /var/log/apache2/error.log | grep "4[0-9][0-9]"'
                sh 'sudo cat /var/log/apache2/error.log | grep "5[0-9][0-9]"'

            }
        }
    }
}

