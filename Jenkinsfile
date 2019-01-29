pipeline {
    agent {
        docker {
			label 'with-gpus'
            image 'nvidia/cuda'
            args  '--runtime=nvidia'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'make -C vectorAdd'
            }
        }
        stage('Test') {
            steps {
                sh 'make -C vectorAdd run'
            }
        }
    }
}
