node {
     stage('HTTP Request') {

                sh '''
                    curl -X GET "https://google.com" \
                         -H "Content-Type: application/json" \
                         -o output.json
                '''
        }
    stage('Clone Express Repository') {
        git url: 'https://github.com/expressjs/express.git'
    }

    stage('npm Install') {
        nodejs() {
                    sh 'npm install'
                }
    }
}
