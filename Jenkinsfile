pipeline {
    agent {
        docker {
			label 'with-gpus'
            image 'nvidia/cuda'
        }
    }
    stages {
        stage('Test') {
            steps {
                sh 'nvidia-smi'
            }
        }
    }
}
