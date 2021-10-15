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
                    echo 'run react-app'
                }
            }
        }

        stage('Deploy') {
            when {
            }
            steps {
                echo 'deploy'
            }
        }
    }
}