pipeline {

    agent any

    stages {

        stage('Build') {
            steps {
                    echo "Building...."
                    sh 'docker build -t tester .'
            }
        }

        stage('Test') {
            steps {
            echo "checking if docker is in the images..."
                    sh 'docker images'
            }
        }

        stage('Deliver') {
            steps {
                    echo "Nothing to do this stage."
            }

            post {
                success {
                        echo "Alas, it has been done."
                }
            }
        }
    }
}
