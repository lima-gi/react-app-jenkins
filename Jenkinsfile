pipeline{
    agent any

    stages {
        stage('Install') {
            steps{
                nodejs(nodeJSInstallationName: 'Node 14.18.1') {
                    sh 'npm install'
                }
            } 
        }
        stage('Build'){
            steps{
                nodejs(nodeJSInstallationName: 'Node 14.18.1') {
                    sh 'npm build'
                }
            }
        }

        stage('Test') {
            steps{
                nodejs(nodeJSInstallationName: 'Node 14.18.1') {
                    sh 'npm start'
                }
            }
        }

        stage('Deploy') {
            when {
                branch 'master'
            }
            steps {
                echo 'deploy'
            }
        }
    }
}