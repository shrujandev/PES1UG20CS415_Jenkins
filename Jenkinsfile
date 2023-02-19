pipeline {
    agent any

    stages {
        stage('Pre Build') {
            steps {
                git branch: 'main',
                url: 'https://github.com/shrujandev/PES1UG20CS415_Jenkins.git'
            }
        }
        stage('Build'){
            steps {
                sh 'make -C test_pipeline'
                echo '[JENKINS PIPELINE] : Build done!'
            }
        }
        stage('Test'){
            steps {
                s '/var/jenkins_home/workspace/PES1UG20CS415/test_pipeline/test_exec'
                echo '[JENKINS PIPELINE] : Test done!'
            }
        }
        stage('Deploy'){
            steps {
                echo '[JENKINS PIPELINE] : PIPELINE EXECUTED DONE!!'
            }
        }
    }
    post {
        failure {
            echo '[JENKINS PIPELINE] : PIPELINE failed'
        }
    }
}
