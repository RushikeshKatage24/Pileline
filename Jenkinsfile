pipeline{
	agent any 
		stages{	
			stage('one'){
					step{
					echo 'Hi, this is Rushikesh from AIT YCP'
					}
					}
			}
			stage('Two'){
					steps{ 
						input( ' Do you want to proceed ?' )
						}
					}
			stage(' Three '){
		when{
			not{
				branch "Master"
				}
			}
			steps{
				echo "Hello"
				}
			}
			
			stage('Four'){
			parallel{
				stage(' Unit Test '){
						steps{
							echo " Running the unit test... "
							}
						}
				stage(' Integration test '){
							agent{
								docker{
									reuseNode false
									imgae 'ubuntu'
									}
								}
							steps{
								echo ' running the integration test ... '
								}
							}
							}
}
}
}
