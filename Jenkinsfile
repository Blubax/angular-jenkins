String testString = "Hello world"

def workspace;

node {
    stage('Checkout') {
        echo "Checking out..."
        checkout([
            $class: 'GitSCM',
            branches: [[name: '*/master']],
            doGenerateSubmoduleConfigurations: false,
            extensions: [],
            submoduleCfg: [],
            userRemoteConfigs: [[
                credentialsId: 'e07ebce5-0c72-4219-b93d-85ee05371012',
                url: 'https://github.com/Blubax/angular-jenkins.git'
            ]]
        ])
        workspace = pwd()
    }

    stage('Build') {
        echo "Building..."
    }

    stage('Test') {
        echo "Testing..."
    }

    stage('Deploy') {
        echo "Deploying... -> TestString: ${testString}"
}
