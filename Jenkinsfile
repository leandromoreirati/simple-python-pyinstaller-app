pipeline {
    agent none
    stages {
        /*stage ('Clean Workspace'){
            steps {
                cleanWs()
            }

        }*/
        stage ('ID do usuarui'){
            steps {
                sh 'id'
            }

        }
        stage ('Build') {
            agent {
                docker {
                    image 'python:2-alpine'
                }
            }
            steps {
                sh 'python -m py_compile sources/add2vals.py sources/calc.py'
            }

        }
    }
}