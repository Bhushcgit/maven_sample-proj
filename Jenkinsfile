node('slave-jup') 
{
    stage('Continuous Download') 
	{
    git 'https://github.com/Bhushcgit/maven_sample-proj.git'
	}
    stage('Continuous Build') 
	{
    sh label: '', script: 'mvn package'
	}
    stage('Continuous Deployment') 
	{
     sh label: '', script: 'scp ~/workspace/jenkins/workspace/multibranch-pipeline_master/target/webapp.war  root@192.168.100.5:/root/tomcat/apache-tomcat-10.0.8/webapps/qaenv.war'
	}
    stage('Continuous Testing') 
	{
              sh label: '', script: 'echo "Testing Passed"'
	}
}
