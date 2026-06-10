pipeline {
    agent none

    stages {

        stage('Clone Code') {
            agent any
            steps {
                git 'https://github.com/pujaraamen/jenkins44.git'
            }
        }

        stage('Deploy on Both Agents') {
            parallel {

                stage('Agent1 Deploy') {
                    agent { label 'dockeragent1' }
                    steps {
                        sh '''
                        echo "Deploying on Agent1"
                        hostname

                        docker rm -f mysite || true
                        docker build -t mysite .
                        docker run -d -p 8081:80 --name mysite mysite
                        '''
                    }
                }

                stage('Agent2 Deploy') {
                    agent { label 'dockeragent2' }
                    steps {
                        sh '''
                        echo "Deploying on Agent2"
                        hostname

                        docker rm -f mysite || true
                        docker build -t mysite .
                        docker run -d -p 8082:80 --name mysite mysite
                        '''
                    }
                }

            }
        }
    }
}
