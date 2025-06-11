pipeline {
    agent any

    parameters {
        string(name: 'CLIENT_ID', defaultValue: '3mf.sb.amp.vg', description: 'Enter client identifier')
    }

    stages {
        stage('Print config.xml') {
            steps {
                script {
                    echo "Client ID: ${params.CLIENT_ID}"
                    def parts = params.CLIENT_ID.tokenize('.')
                    def filePath = "config_samples/${parts.join('/')}/config.xml"
                    echo "Resolved path: ${filePath}"

                    if (fileExists(filePath)) {
                        def fileContent = readFile(filePath)
                        echo "======== config.xml content ========"
                        echo fileContent
                        echo "===================================="
                    } else {
                        error "config.xml not found at ${filePath}"
                    }
                }
            }
        }
    }
}
