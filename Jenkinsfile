pipeline {
    agent any
    stages {
        stage('Example') {
            steps {
                script {
                    // Access parameters using the 'params' object
                    def browserName = params.browserName
                    def testSuitePath = params.testSuitePath
                    def executionProfile = params.executionProfile

                    cd /Applications/Katalon\ Studio\ Engine.app/Contents/MacOS
                    echo './katalonc -retry=0 -testSuitePath="${testSuitePath}" -browserType="${browserName}" -executionProfile="${executionProfile}" -apiKey="6067c065-a8eb-44c1-b724-e1851ab5fe0e" -orgID=200326 --config -proxy.auth.option=NO_PROXY -proxy.system.option=NO_PROXY -proxy.system.applyToDesiredCapabilities=true -webui.autoUpdateDrivers=true'
                    ./katalonc -retry=0 -testSuitePath="${testSuitePath}" -browserType="${browserName}" -executionProfile="${executionProfile}" -apiKey="6067c065-a8eb-44c1-b724-e1851ab5fe0e" -orgID=200326 --config -proxy.auth.option=NO_PROXY -proxy.system.option=NO_PROXY -proxy.system.applyToDesiredCapabilities=true -webui.autoUpdateDrivers=true
                }
            }
        }
    }
}
