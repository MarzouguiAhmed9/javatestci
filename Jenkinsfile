pipeline {
    agent any

    stages {
        stage('clone') {
            steps {
                sh "rm -rf *"
                sh "git clone https://github.com/MarzouguiAhmed9/javatestci.git"
            }
        }

         stage('build') {
            steps {
                sh "cd javatestci/src / && javac Main.java"
            }
        }

         stage('run') {
            steps {
                  sh "cd javatestci/src / && java Main.java"            }
        }
    }
}
