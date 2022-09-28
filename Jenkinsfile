@Library("shared-library")_
pipeline {
    agent any
    
    tools{
        nodejs 'nodejs'
    }
    
    environment {
        PROJECT_ROOT = 'angular-app'
        REGISTRY = 'priscillajb/nodeapp'
    }
    
    stages{

		stage('Install'){
            steps{
				Dependencies(project_root:PROJECT_ROOT)
            }
    }

    	stage('Build'){
            steps{
                Build(project_root:"${PROJECT_ROOT}",registry:"${REGISTRY}",buildNumber:"${BUILD_NUMBER}")
            }
    }
}
}
