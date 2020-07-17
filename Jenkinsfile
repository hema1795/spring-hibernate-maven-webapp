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
}
