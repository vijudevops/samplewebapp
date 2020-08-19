pipeline {
        agent any
        stages{
                    stage ('Build')
                    {
                                    steps
                                        {
                                            git url: 'https://github.com/vijudevops/samplewebapp.git'
                                            sh 'docker build -t samplewebapp:v1.1.0 .'
                                        }
                    }
                    stage ('Deploy')
                    {
                                    steps
                                        {
                                            sh 'docker run -d -p 9081:80 samplewebapp:v1.1.0 --name nginxServic --restart=\'always\''
                                        }
                    }
              }    
}
