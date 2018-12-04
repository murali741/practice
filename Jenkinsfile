#!/usr/bin/env groovy

pipeline {
    agent any
	
	parameters{
	     string(defaultValue: true, description: '', name: 'source_branch')
		 string(defaultValue: true, description: '', name: 'feature_branch')
		 string(defaultValue: true, description: '', name: 'date(mmyy)')
		 string(defaultValue: true, description: '', name: 'jira ticket number')
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
