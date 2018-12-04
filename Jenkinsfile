#!/usr/bin/env groovy

pipeline {
    agent any
	
	parameters{
	     string(defaultValue: 'develop', description: '', name: 'source_branch')
		 string(defaultValue: 'none', description: '', name: 'feature_branch')
		 string(defaultValue: 'none', description: '', name: 'date(mmyy)')
		 string(defaultValue: 'none', description: '', name: 'jira ticket number')
	}

    stages {
        stage('conflict') {
            steps {
                sh 'cd tools'
                sh './submodule-sync '
            }
        }
    }
}
