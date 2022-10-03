pipeline{
	agent {
	label {
		label 'slave'
		customWorkspace '/git'
		}
	}
          stages {
		stage ('install-httpd') {
			steps {
				sh "sudo yum install httpd -y"
				}
			}
		stage ('service start') {
                        steps {
                                sh "sudo service httpd start"
                                }
                        }
		stage ('copy index') {
                        steps {
                                sh "sudo cp -r /git/index.html /var/www/html"
                                }
                        }
		}
	}
