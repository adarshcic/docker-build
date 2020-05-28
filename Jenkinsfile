pipeline {

    agent any

    stages {
        stage('Deploy') {
            steps {
                script {
                    openshiftBuild(namespace: 'don-elk-stack', buildConfig: 'myapp', showBuildLogs: 'true')
                }
            }
        }
    }
}
