pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Validate Project Files') {
            steps {
                sh '''
                    set -eu
                    test -s README.md
                    test -s kubernetes/prometheus-values.yaml
                    echo "Project files are present."
                '''
            }
        }

        stage('Validate Prometheus Configuration') {
            steps {
                sh '''
                    set -eu
                    grep -q "server:" kubernetes/prometheus-values.yaml
                    echo "Prometheus configuration check passed."
                '''
            }
        }
    }

    post {
        success {
            echo 'VLE-7 monitoring project validation succeeded.'
        }
        failure {
            echo 'Project validation failed.'
        }
    }
}
