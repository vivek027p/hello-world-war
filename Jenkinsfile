pipeline {
	agent { label 'slave4' }
    			stages {
        			stage('Checkout') {
            				steps {
					sh "rm -rf /home/slave4/workspace/mavenproj/hello-world-war"	
               				 sh "git clone https://github.com/vivek027p/hello-world-war.git"          					}
       					 }
				stage('Build') {
            				steps {
               				 sh "cd hello-world-war"
						sh "docker build -t vivek027p/hello:1.0 ."
            					}
       					 }
				stage('Publish') {
            				steps {
               				 sh "docker login -u vivek027p -p vivek@123"
						sh "docker push vivek027p/hello:1.0"
            					}
       					 }
				/*stage('Deploy') {
            				steps {
						sh "pwd"
						sh "ls"
		
sh "whoami"
               				 sh "cp /home/slave4/workspace/mavenproj/target/hello-world-war-1.0.0.war /opt/apache-tomcat-9.0.63/webapps/"
            					}
       					 }*/
   				 }
		}
