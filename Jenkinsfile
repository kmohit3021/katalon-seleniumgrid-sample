pipeline {
    agent any
    parameters {
        string(name: 'browserName', defaultValue: '', description: 'Enter browser name')
        string(name: 'testSuitePath', defaultValue: '', description: 'Enter test suite path')
        string(name: 'executionProfile', defaultValue: '', description: 'Enter execution profile')
    }
    stages {
        stage('Example') {
            steps {
                script {
                    def browserName = params.browserName
                    def testSuitePath = params.testSuitePath
                    def executionProfile = params.executionProfile

                    // Change directory and execute Katalon command using sh step
                    sh '''
                        cd /Applications/KatalonStudioEngine.app/Contents/MacOS
                        ./katalonc -retry=0 -testSuitePath="${testSuitePath}" -browserType="${browserName}" -executionProfile="${executionProfile}" -apiKey="6067c065-a8eb-44c1-b724-e1851ab5fe0e" -orgID=200326 --config -proxy.auth.option=NO_PROXY -proxy.system.option=NO_PROXY -proxy.system.applyToDesiredCapabilities=true -webui.autoUpdateDrivers=true
                    '''
                }
            }
        }
    }
}
