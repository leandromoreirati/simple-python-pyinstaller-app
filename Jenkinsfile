pipeline {
    agent none
    stages {
        /*stage ('Clean Workspace'){
            steps {
                cleanWs()
            }

        }*/
        stage ('Build') {
            agent {
                docker {
                    image 'python:alpine3.10'
                }
            }
            steps {
                sh '''
                    python -m py_compile sources/add2vals.py sources/calc.py
                '''
            }

        }
    }
}