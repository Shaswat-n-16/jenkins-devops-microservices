//DECLERATIVE
pipeline{
		agent {docker{Images 'maven:3.6.3'}}
		stages{
			stage('Build'){
				steps{
					sh 'mvn --version' 
					echo "Build"	
				}
			}
			stage('Test'){
				steps{
					echo "Test"		
				}
			}
			stage('Integration Test'){
				steps{
					echo "Integration Test"
				}
			}
		}
			post{
				always{
					echo 'Im awesome, i run always'
				}
				success{
					echo 'I run when you are successful'
				}
				failure{
					echo 'I run when you fail'
				}
			}
		
}
		
