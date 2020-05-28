pipeline {

    agent any

    stages {
        stage('Deploy') {
            openshiftBuild(namespace: 'don-elk-stack', buildConfig: 'myapp', showBuildLogs: 'true')
        }
    }
}
