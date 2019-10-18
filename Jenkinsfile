node('master'){
	   stage('git checkout'){
	                  git 'https://github.com/mythribhay/Inglibraryui'
	              }
	   stage('angular build'){
	             sh 'npm install'
	             sh 'ng build --base-href=/book-management/'
	         }
	
	stage('Frontend deploy'){
	             sh 'cd /var/lib/jenkins/workspace/frontend/dist'
	             sh 'sudo cp -rf book-management /opt/apache-tomcat-9.0.26/webapps/'
	         }
	}
