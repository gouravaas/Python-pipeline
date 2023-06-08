pipeline {
	agent {
		label 'ubuntu-slave'
		}
	stages {
		stage ("pull scm") {
			steps {
				git branch: 'python', url: 'https://github.com/gouravaas/Python-pipeline.git'
				}
			}
		stage ("Build") {
			steps {
				sh 'python3 -V'
				sh 'python3 cp.py'
				}
			}
		stage ("Test") {
			steps {
				sh 'python3 test.py'
				}
			}
		}
	}
