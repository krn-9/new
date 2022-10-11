pipeline {
  agent {
    label {
      label 'built-in'
      customWorkspace '/home/ec2-user/project'
      }
      }
  stages {
    stage ('create-volume'){
      steps {
        sh "docker volume create vol2"
        sh "cp -r /home/ec2-user/project/slave2/index.html /var/lib/docker/volumes/vol2/_data"
          sh "docker run --name cont2 -itdp 90:80 -v vol2:/usr/local/apache2/htdocs httpd"
        }
        }
      }
    }
