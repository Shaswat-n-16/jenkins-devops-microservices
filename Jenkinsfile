//DECLERATIVE
pipeline{
		agent any
		//agent { docker { image 'maven:3.6.3' }}
		enviroment{
			dockerHome=tool 'myDocker'
			mavenHome=tool 'myMaven'
			PATH="$dockerHoe/bin:$mavenHome/bin:$PATH"
		}
		stages{
			stage('Build'){
				steps{
					sh 'mvn --version' 
					sh 'docker --version'
					echo "Build"	
					echo "PATH - $PATH"
					echo "BUILD_NUMBER - $env.BUILD_NUMBER"
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
		
