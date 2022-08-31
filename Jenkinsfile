pipeline {
  agent any {
          tools { maven “MAVEN_HOME” }
          stages {
                  stage ( ‘taking code from git ’ )
                        {
                         steps {
                                git branch : master,
                                credentialsId: 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,
                                url: https://github.com/tanishqsharma00/hello-world.git
                               }
                        }
                 stage ( ' build ' )
                       {
                         steps {
                                ‘mvn -B -DskipTests clean package’
                              }
                       }
                stage ( ' deploy ’)
                      {
                        steps {
                             sh ‘cp -ivr /opt/tomcat/.jenkins/workspace/project_java_16/target/udit.war  /opt/tomcat/webapps’
                             }
                      }
          }
  }
