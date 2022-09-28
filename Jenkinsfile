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
     sh label: '', script: 'scp ~/workspace/jenkins/workspace/multibranch-pipeline_master/target/*jar  root@192.168.100.5:/root/tomcat/apache-tomcat-10.0.8/webapps/'
	}
    stage('Continuous Testing') 
	{
               sh 'java -cp target/my-app-1.0-SNAPSHOT.jar com.mycompany.app.App >result.txt'
		sh 'cat result.txt'
		sh label: '', script: 'echo "Testing Passed"'
	}
}
