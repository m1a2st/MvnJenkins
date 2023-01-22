pipeline {
    agent any
    stages {
        stage('clone repo') {
            steps {
                sh "rm -rf MvnJenkins"
                sh "git clone https://github.com/m1a2st/MvnJenkins.git"
                sh "mvn clean -f MvnJenkins"
            }
        }
        stage('test'){
            steps{
                sh "mvn test -f MvnJenkins"
            }
        }
        stage('Display'){
            steps{
                sh "mvn package -f MvnJenkins"
            }
        }
    }
}
