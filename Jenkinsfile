node{
stage('SCM checkout')
{ 
git'https://github.com/hema1795/spring-hibernate-maven-webapp'
}
stage('clean')
{
  def mvnHome = tool name: 'maven3', type: 'maven'
  sh " ${mvnHome}/bin/mvn clean install package"
}
  stage('deploy')
  {
   sshagent(['tomcat.dev']) {
    sh 'scp -o StrictHostKeyChecking=no target/*.war ubuntu@13.233.60.237'
}
  }
}
