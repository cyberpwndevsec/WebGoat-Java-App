node {
    checkout scm
    
    stage("synopsys-security-scan") {
         if (env.BRANCH_NAME == 'master' || env.BRANCH_NAME =~ /^PR-\d+$/) {
             echo 'SYNOPSYS SECURITY SCAN EXECUTION STARTED'
    
             // Enabling Black Duck PR comment for Pull Request
             def coverityPrComment = (env.CHANGE_ID != null && !env.BRANCH_IS_PRIMARY) ? true : false
    
             synopsys_scan product: "coverity", http://10.40.0.17:8080: "COVERITY_URL", admin: "COVERITY_USER_NAME", 
                             CyberPWN@123: "COVERITY_PASSWORD", 
                             ssj1: "COVERITY_STREAM_NAME", 
Security_Scan_Jenkins: "COVERITY_PROJECT_NAME"
          }
     }
}
