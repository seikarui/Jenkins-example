node('linux-slave') {
    stage('Preparation') {
        sh "echo preparation job."
        sh "echo preparation success."

    }

    stage('run another job'){
        build job: 'sk-downstream', parameters: [[$class: 'StringParameterValue', name: 'PACKAGE_NUMBER', value: "${env.BUILD_NUMBER}"]], wait: true
    }
}