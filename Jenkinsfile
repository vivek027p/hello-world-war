pipeline {
	agent { label 'slave4' }
    			stages {
        			stage('Checkout') {
            				steps {
					sh "rm -rf /home/slave4/workspace/testmulti/hello-world-war"	
               				 sh "git clone https://github.com/vivek027p/hello-world-war.git"
            					}
       					 }
				stage('Build') {
            				steps {
               				 sh "mvn clean package"
            					}
       					 }
				stage('Deploy') {
            				steps {
						sh "pwd"
						sh "ls"
		
sh "whoami"
               				 sh "cp /home/slave4/workspace/testmulti/target/hello-world-war-1.0.0.war /opt/apache-tomcat-9.0.62/webapps/"
            					}
       					 }
   				 }
		}
