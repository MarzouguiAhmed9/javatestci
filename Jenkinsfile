pipeline {
    agent any 

    stages {
        stage("Build") {
            steps {
                // Navigate to the src directory and compile the Java file
                sh '''
                cd src
                javac Main.java
                '''
            }
        }

        stage("Run") {
            steps {
                // Run the compiled Java program
                sh '''
                cd src
                java Main
                '''
            }
        }
    }
}
