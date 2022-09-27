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
}
