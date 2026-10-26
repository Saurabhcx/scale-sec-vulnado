pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/Saurabhcx/scale-sec-vulnado.git',
                    branch: 'master',
                    credentialsId: 'Git-saurabh-test'
            }
        }
        
        stage('SAST Scan - Checkmarx One') {
            steps {
             checkmarxASTScanner additionalOptions: '--debug', baseAuthUrl: 'https://ind.iam.checkmarx.net/', branchName: 'master', checkmarxInstallation: 'CxOne-CLI', credentialsId: '', projectName: 'Saurabhcx/scale-sec-vulnado', serverUrl: 'https://ind.ast.checkmarx.net/', tenantName: 'Testing15'
            }
        }
    }
}
