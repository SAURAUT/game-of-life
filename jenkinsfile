node {
		stage ('SCM') {
		git 'https://github.com/SAURAUT/game-of-life.git'
		}
		
		stage ('build packages') {
		sh 'mvn package'
		}
		
		stage ('Junit test results') {
        junit 'gameoflife-web/target/surefire-reports/*.xml'  
        }
        
		stage ('archival') {
        archiveArtifacts 'gameoflife-web/target/*.war'		
		}
		
		
	}
