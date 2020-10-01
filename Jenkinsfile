pipeline {
    agent any
    stages {
        stage('Git Checkout') {
            steps {
                checkout([
                    $class: 'GitSCM',
                    branches: [[name: '$GIT_BRANCH']],
                    doGenerateSubmoduleConfigurations: false,
                    extensions: [[$class: 'RelativeTargetDirectory', relativeTargetDir: '.']],
                    submoduleCfg: [],
                    userRemoteConfigs: [[url: 'https://github.com/Chi996/jenkins-test-project3.git']]
                ])
                bat 'echo Checking out the scripts repository $GIT_BRANCH'
                bat 'dir'
            }
        }
    }
}
