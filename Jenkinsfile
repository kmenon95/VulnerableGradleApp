pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Snyk Scan') {
            steps {
                // Run Snyk Security scan
                snykSecurity(
                    failOnError: false,
                    organisation: '70662de2-e4ea-48c8-97b8-d0bff5b677ad',
                    severity: 'high',
                    snykInstallation: 'Snyk_Install',
                    snykTokenId: 'SnykAPI'
                )
            }
        }
    }
}
