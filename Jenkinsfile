pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
               
                echo 'Build'
                              
            }
        }
        stage('Change_Stage') {
            steps {
                //snDevOpsChange changeCreationTimeOut: 40, changeRequestDetails: '{ "attributes": { "short_description": "Test description", "priority": "1", "start_date": "2021-02-05 08:00:00", "end_date": "2022-04-05 08:00:00", "justification": "test justification", "description": "test description", "cab_required": true, "comments": "This update for work notes is from jenkins file", "work_notes": "test work notes", "assignment_group": "a715cd759f2002002920bde8132e7018" }, "setCloseCode": false }', changeStepTimeOut: 60, pollingInterval: 5
                echo 'change with timeout'
                //snDevOpsGetChangeNumber //changeDetails: '{ "pipeline_name": "divya-pipeline-2", "build_number": '${env.BUILD_NUMBER}', "stage_name": "Change_Stage"}'
        }
        }
        stage('Get_Change') {
            steps {
                  //  snDevOpsUpdateChangeInfo(changeRequestDetails: """{"state":"4","reason":"Location changed", "description": "Canceling change as Location changed from ${currStageName} Step by ${env.BUILD_NUMBER}", "comments": "Update of change request through Update API from ${currStageName} Step by ${env.BUILD_NUMBER}", "work_notes": "Update of change request through Update API from ${currStageName} Step by ${env.BUILD_NUMBER}"}""", changeRequestNumber: """${changeRequestNumber}""")
                    snDevOpsUpdateChangeInfo changeRequestDetails: '{ "short_description": "Test description", "priority": "1", "start_date": "2021-02-05 08:00:00", "end_date": "2022-04-05 08:00:00", "justification": "test justification", "description": "test description", "cab_required": true, "comments": "This update for work notes is from jenkins file", "work_notes": "test work notes", "assignment_group": "a715cd759f2002002920bde8132e7018"}', changeRequestNumber: 'CHG000001'
            }
        }//End of Get_Change
    }
}
