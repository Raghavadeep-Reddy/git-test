pipeline {
    agent any
    stages {
        stage('One') {
                steps {
                        echo 'Hi, this is Raghavadeep Reddy'
			sh 'date'
			
                }
        }
	    stage('Two'){
		    
		steps {
			echo 'This is Stage Two'
        }
	    }
        stage('Three') {
                when {
                        not {
                                branch "master"
                        }
                }
                steps {
			echo "Hello World"
                        }
        }
        stage('Four') {
                parallel {
                        stage('Unit Test') {
                                steps{
                                        echo "Running the unit test..."
                                }
                        }
                        stage('Integration test') {
                        
				steps {
					echo 'Running the integration test..'
				}
                               
			}  }
        }
    }
}

