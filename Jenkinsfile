pipeline {
    agent {
        node {
            label 'nodejs'
        }
    }
    stages {
	stage('Run Tests') {
            parallel {
                stage('Backend Tests') {
                    steps {
                        sh 'node ./backend/test.js'
                    }
                }
                stage('Frontend Tests') {
                    steps {
			echo "Frontend Tests"
                        sh 'node ./frontend/test.js'
                    }
                }
            }
        }
    }
}
