#!groovy

node {
    stage('configFile Plugin') {
        sh 'npm install'
        sh 'gradle build -p android -x lint'
    }
    stage('notify') {
        def ac = ArtifactConfig('1', '2')
        uploadToIncappticConnect token: 'a', url: 'b', artifactConfigList: [ac]
    }
}
