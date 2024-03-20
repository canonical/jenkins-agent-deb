pipeline {
    agent none

    stages {
        stage('Build') {
            agent { label 'machine' }

            steps {
                sh'''#!/bin/bash
                    echo "$(hostname) $(date) : Running in $(pwd) as $(whoami)"
                    debuild -us -uc
                '''
            }
        }
    }
}
