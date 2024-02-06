pipeline {
    agent any
    parameters {
        // Define parameters here, matching the names in Jenkins job configuration
        string(name: 'browserName', defaultValue: 'Remote', description: 'Enter your username')
        string(name: 'testSuitePath', defaultValue: 'Test Suites/TS001_Web', description: 'Enter your TestSuite Path')
        choice(name: 'executionProfile', choices: ['default', 'qa', 'prod'], description: 'Select environment profile')
    }
    stages {
        stage('Example') {
            steps {
                script {
                    // Access parameters using the 'params' object
                    def browserName = params.browserName
                    def testSuitePath = params.testSuitePath
                    def executionProfile = params.executionProfile
                    
                    // Use the parameters in your pipeline
                    cd /Applications/Katalon Studio Engine.app/Contents/MacOS
                    ./katalonc -retry=0 -testSuitePath="$testSuitePath" -browserType="$browserName" -executionProfile="$executionProfile" -apiKey="6067c065-a8eb-44c1-b724-e1851ab5fe0e" -orgID=200326 --config -proxy.auth.option=NO_PROXY -proxy.system.option=NO_PROXY -proxy.system.applyToDesiredCapabilities=true -webui.autoUpdateDrivers=true
                }
            }
        }
    }
}
