pipeline {

    agent any

    stages {
        stage('Deploy') {
            steps {
                script {
                    openshiftBuild(namespace: "${MY_NAMESPACE}", buildConfig: 'myapp', showBuildLogs: 'true')
                    openshiftTag(srcStream: "${MY_REGISTRY}", srcTag: 'latest', destStream: 'graphtool', destTag: 'latest', namespace: "${MY_NAMESPACE}", destinationNamespace: "${MY_NAMESPACE}")

                }
            }
        }
    }
}
