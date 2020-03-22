pipeline {
    agent none
    environment {
        BUILD_WITH_CONTAINER = '0'
    }
    stages {
        stage('Build Istio') {
             agent {
                docker {
                    label 'docker'
                    image 'gcr.io/istio-testing/build-tools:release-1.4-2020-01-06T22-39-32'
                }
            }

            steps {
                checkout scm
                sh '''#!/bin/bash
                make

                '''

            }
        }
    }
}
