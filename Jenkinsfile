 @Library('pipeline-library-demo')_
node {
    stage('SCM') {
	echo 'Gathering code from version control'
    }
    stage('Build') {
        echo 'Building....'
         rlsnotes()
    }
    stage('Test') {
        echo 'Testing....'
    }
    stage('Deploy') {
        echo 'Deploying....'
    }
}
