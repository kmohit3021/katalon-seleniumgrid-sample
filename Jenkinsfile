pipeline {
    agent any
    parameters {
        string(name: 'browserName', defaultValue: '', description: 'Enter your browser name')
        choice(name: 'executionProfile', choices: ['default', 'qa', 'prod'], description: 'Select your environment profile')
        string(name: 'testSuitePath', defaultValue: '', description: 'Enter your test suite path')
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
                        cd '/Applications/Katalon Studio Engine.app/Contents/MacOS'
                        ./katalonc -noSplash -runMode=console -projectPath="/Users/mohit/Katalon Studio/katalon-seleniumgrid-sample/katalon-seleniumgrid-sample.prj" -retry=0 -testSuitePath="${testSuitePath}" -browserType="${browserName}" -executionProfile="${executionProfile}" -apiKey="${apiKey}" -orgID=${orgID} --config -proxy.auth.option=NO_PROXY -proxy.system.option=NO_PROXY -proxy.system.applyToDesiredCapabilities=true -webui.autoUpdateDrivers=true
                    '''
                }
            }
        }
    }
}
