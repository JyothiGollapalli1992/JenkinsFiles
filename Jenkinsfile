node
{

def mavenHome= tool name: 'maven3.6.2'

stage('CheckoutCode')

{

git branch: 'development', credentialsId: '92422177-8e69-4024-a057-1c227cc08130', url: 'https://github.com/JyothiGollapalli1992/maven-web-application.git'


}

stage('Build')

{

sh "${mavenHome}/bin/mvn clean package"

}
/*
stage('sonarQubeReportExecution')

{

sh "${mavenHome}/bin/mvn sonar:sonar"

}

stage('UploadArtifactsIntoNexus')

{
sh "${mavenHome}/bin/mvn clean deploy"

}

stage('DeployAppIntoTomcat')

{

sshagent(['898f6224-5faa-4c8e-bbf2-bb7e6c6a5ab9'])

{
  
sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@35.154.188.109:/opt/apache-tomcat-9.0.34/webapps/"

}

}

stage('EmailNotification')

{
emailext body: '''build is over

RD,
Jyo.''', subject: 'hi', to: 'jyothigece2@gmail.com'

}

*/

}
