pipeline {
  agent {
    label {
      label 'built-in'
      customWorkspace '/home/ec2-user/project/slave1'
      }
      }
  stages {
    stage ('create-volume'){
      steps {
        sh "docker volume create vol1"
        sh "cp -r /home/ec2-user/project/slave1/index.html /var/lib/docker/volumes/vol1/_data"
          sh "docker run --name cont1 -itdp 80:80 -v vol1:/usr/local/apache2/htdocs httpd"
        }
        }
      }
    }
