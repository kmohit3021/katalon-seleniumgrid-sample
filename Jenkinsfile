pipeline {
    agent any
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
