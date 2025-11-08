pipeline {
   agent any
   stages {
        stage('First') {
            steps {
                echo "Branch name: ${env.BRANCH_NAME}"
            }
        }
        stage('Second') {
	    when {
                branch 'main'
            }
            steps {
                echo 'Jenkins, do something.'
		sh '''                
		df -h
 		echo ""
		echo "This is build id ${BUILD_ID}."
		echo "\$ is a dollar sign."
		date > the_now.txt
		cat the_now.txt
		'''
            }
        }
        stage('Thoid') {
            when {
                branch 'uggabooga'
            }
            steps {
                echo 'Jenkins, do some stuff.'
                echo 'Dis is branch uggabooga'
            }
        }
	   stage('Foah') {
		   when {
			   branch 'main'
		   }
		   steps {
			   echo 'This executed because this is the main branch.'
		   }
	   }
    }
}
