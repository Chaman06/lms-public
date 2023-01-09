pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'cd webapp && npm install'
                sh 'cd webapp && npm run build'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying......'
		sh 'scp -r webapp/dist ubuntu@http:65.2.70.155:/var/www/html/'
            }
        }
    }
}
