pipeline{
	agent any
	stages{
        stage('Clone Repository'){
					steps{
						checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'github-id', url: 'https://github.com/etechteam3group5/conditional-mult-pipeline.git']]])
					}
				}
		stage('parallel-level1'){
            when {
                branch 'feature'
            }
			parallel{
				stage('Max'){
					steps{
						echo "sub-job1 tasks and commands and actions"
						sh "lscpu"
                        sh "sudo systemctl status jenkins"
					}
				}
				stage('Chima'){
					steps{
						echo "sub-job2 tasks and commands and actions"
						sh "lscpu"
                        sh "sudo systemctl status jenkins"
					}
				}
			}
		}
        stage('parallel-leve2'){
            when {
                branch 'develop'
            }
			parallel{
				stage('Chizoba'){
					steps{
						echo "sub-job3 tasks and commands and actions"
						sh "lscpu"
                        sh "sudo systemctl status jenkins"
					}
				}
				stage('Christiana'){
					steps{
						echo "sub-job4 tasks and commands and actions"
						sh "lscpu"
                        sh "sudo systemctl status jenkins"
					}
				}
			}
		}
        stage('parallel-level3'){
            when {
                branch 'main'
            }
			parallel{
				stage('Gregory'){
					steps{
						echo "sub-job5 tasks and commands and actions"
						sh "lscpu"
                        sh "sudo systemctl status jenkins"
					}
				}
				stage('Tunde'){
					steps{
						echo "sub-job6 tasks and commands and actions"
						sh "lscpu"
                        sh "sudo systemctl status jenkins"
					}
				}
			}
		}
        stage('parallel-level4'){
             when {
                branch 'main'
            }
			parallel{
				stage('Valentine'){
					steps{
						echo "sub-job7 tasks and commands and actions"
						sh "lscpu"
                        sh "sudo systemctl status jenkins"
					}
				}
				stage('Wasiu'){
					steps{
						echo "sub-job8 tasks and commands and actions"
						sh "lscpu"
                        sh "sudo systemctl status jenkins"
					}
				}
			}
		}
		stage('End of Pipeline'){
			steps{
				echo "end of parallel job"
			}
		}
	}	
}
