pipeline{
    agent any

    stages {
        stage('Install') {
            steps{
                nodejs(nodeJSInstallationName: 'Node 14.18.1') {
                    sh 'npm install'
                }
            }
            echo 'install packages'
        }
        stage('Build'){
            steps{
                nodejs(nodeJSInstallationName: 'Node 14.18.1') {
                    sh 'npm build'
                }
            }
            echo 'react build'
        }

        stage('Test') {
            steps{
                nodejs(nodeJSInstallationName: 'Node 14.18.1') {
                    sh 'npm start'
                }
            }
            echo 'react run'
        }

        stage('Deploy') {
            when {
                branch 'master'
            }
            echo 'Deploy'
        }
    }
}