pipeline {
    agent any

    stages {
        stage('Compile') {
            steps {
                echo 'build has to been started'
		bat 'atlas-compile'
            }
        }
	stage('Package') {
            steps {
                echo 'packaging has to been started'
		bat 'atlas-package'
            }
        }
	stage('Deploy') {
            steps {
		echo 'Deployment started'
                bat 'atlas-install-plugin --username rangamedisetti423 --password Jira@423 --server localhost --http-port 8080 		--plugin-key com.atlassian.jira.jira-api --context-path ""'
            }
        }
    }
}
