def branch
pipeline {
    agent none
    stages {
        stage('test') {
            steps {
                script {
                    echo "Testing the application..."
                    echo "Executing pipeline for branch $BRANCH_NAME"
                    }
                }
            }
        stage('build') {
            when {
                expression{
                    BRANCH_NAME == 'master'
                }
            }
            
            steps {
                script {
                    echo "building the application..."
                    }
                }
            
        }
        stage('deploy') {
            when {
                expression{
                    BRANCH_NAME == 'master'
                }
                
            steps {
                script {
                    echo "deploying the application..."
                    }
                }
            
            }

    }
 
    }
}
