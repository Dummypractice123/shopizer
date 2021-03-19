pipeline {
    agent any
    stages {
        stage('Source') {
            steps {
                git 'https://github.com/Dummypractice123/shopizer.git'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn package'
            }
        }
        stage('PostBuild') {
            steps {
                archiveArtifacts artifacts: 'sm-core/target/*.jar', followSymlinks: false
            }
        }
    }
}
