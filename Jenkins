pipeline {
agent any

environment {
    APP_NAME    = "test-App"
    APP_VERSION = "1.0.0"
    APP_ENV     = "dev"
}

stages {
    stage('Build') {
        steps {
            echo "Building application..."
            echo "Building APP name: ${APP_NAME}"
            echo "Building APP version: ${APP_VERSION}"
            echo "Building APP Environment: ${APP_ENV}"
        }
    }

    stage('Test') {
        steps {
            echo "Running tests on APP: ${APP_NAME}, version: ${APP_VERSION}, environment: ${APP_ENV}"
        }
    }

    stage('Deploy') {
        steps {
            echo "Deploying APP: ${APP_NAME}, version: ${APP_VERSION}, environment: ${APP_ENV}"
        }
    }
}

post {
    success {
        echo "Pipeline is successful"
    }
    failure {
        echo "Pipeline has failed"
    }
    always {
        echo "This will always run"
    }
}

}
