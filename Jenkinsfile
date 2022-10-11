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
        sh "docker volume create vol3"
        sh "cp -r /home/ec2-user/project/slave3/index.html /var/lib/docker/volumes/vol3/_data"
          sh "docker run --name cont3 -itdp 8090:80 -v vol2:/usr/local/apache2/htdocs httpd"
        }
        }
      }
    }
