pipeline {
    agent any 

    stages {
        stage("Build") {
            steps {
                script {
                    // Correcting the path: no 'javatestci' directory, just 'src'
                    sh 'cd src && javac Main.java'
                }
            }
        }

        stage("Run") {
            steps {
                script {
                    // Correcting the path again for running the program
                    sh 'cd src && java Main'
                }
            }
        }
    }

    post {
        always {
            script {
                deleteDir() // Clean up the workspace after the build
            }
        }
    }
}
