node
{
  echo "GitHub BranhName ${env.BRANCH_NAME}"
  echo "Jenkins Job Number ${env.BUILD_NUMBER}"
  echo "Jenkins Node Name ${env.NODE_NAME}"
  
  echo "Jenkins Home ${env.JENKINS_HOME}"
  echo "Jenkins URL ${env.JENKINS_URL}"
  echo "JOB Name ${env.JOB_NAME}"
  
  properties([
    buildDiscarder(logRotator(numToKeepStr: '3')),
    pipelineTriggers([
        pollSCM('* * * * *')
    ])
  ])
  
    def mavenHome = tool name:"maven-3.6.2"
    
stage('checkout')
{
git 'https://github.com/gajjalareddy7012/maven-web-application.git'
}
  /*
stage ('Build')
{
    sh "${mavenHome}/bin/mvn clean package"
    
}

stage ('sonarqube Report')
{
    sh "${mavenHome}/bin/mvn sonar:sonar"
}

stage('uploadartifactoryintonexus')
{
    sh "${mavenHome}/bin/mvn deploy"
    
}

stage('Deploymentinto tomcat')
{
    sshagent(['4e798b25-77e5-406f-8656-b87fdb290ec3'])
    {
    sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@13.233.97.96:/opt/apache-tomcat-9.0.30/webapps/"

    }
    
    stage ('sendEmailNotification')
    {
        emailext body: '''Buils is Successful..
    
    Regards,,
      Aravind Reddy
      7348802800''', subject: 'Buils is Successful', to: 'satishswarna01@gmail.com'
    }
}
*/
}
