 @Library('pipeline-library-demo')_
node {
    stage('SCM') {
	echo 'Gathering code from version control'
    }
    stage('Build') {
        echo 'Building....'
         //rlsnotes()
	   releasenotes()
    }
    stage('Test') {
        echo 'Testing....'
    }
    stage('Deploy') {
        echo 'Deploying....'
    }
}
