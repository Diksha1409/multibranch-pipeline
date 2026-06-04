pipeline {
          agent {
                  label "built-in"
                }
          stages {
              stage("install-httpd"){
                steps {
                        sh "yum install httpd -y"
                      }
                     }
              stage("start-httpd"){
                 steps {
                         sh "systemctl start httpd"
                       }
                     }
              stage("deploy-httpd"){
                 steps {
                         sh "chmod -R 777 /var/www/html/index.html"
                         sh "cp -r index.html /var/www/html/index.html"
                        }
                      }
                  }
           }
