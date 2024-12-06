pipeline {
    agent any 

    stages {
        stage("build") {
            steps {
                script {
                    sh 'cd javatestci/src && javac Main.java'
                }
            }
        }

        stage("run") {
            steps {
                script {
                    sh 'cd javatestci/src && java Main'
                }
            }
        }
    }

    post {
        always {
            script {
                deleteDir()
            }
        }
    }
}
