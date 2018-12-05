#!/usr/bin/env groovy

pipeline {
    agent any
        parameters{
             string(defaultValue: 'develop', description: '', name: 'source_branch')
                 string(defaultValue: 'none', description: '', name: 'feature_branch')
                 string(defaultValue: 'none', description: '', name: 'date')
                 string(defaultValue: 'none', description: '', name: 'jira_ticket')
                 gitParameter branchFilter: 'origin/(.*)', defaultValue: 'master', name: 'BRANCH', type: 'PT_BRANCH'
            }
    stages {
        stage('conflict') {
            steps {
                git branch: "${params.BRANCH}", url: 'https://github.com/murali741/practice.git'
                dir('tools') {
 		   sh 'tools/test.sh'
		}
            }
        }
    }
}
