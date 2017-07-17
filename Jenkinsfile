node {
    checkout([
         $class: 'GitSCM',
         branches: scm.branches,
         doGenerateSubmoduleConfigurations: scm.doGenerateSubmoduleConfigurations,
         extensions: scm.extensions + [
             [
                 $class: 'UserIdentity',
                 email: 'jenkins@example.com',
                 name: 'jenkins'
             ], [
                $class: 'PreBuildMerge',
                options: [
                    mergeRemote: 'origin',
                    fastForwardMode: 'FF',
                    mergeTarget: 'master'
                ]
            ]
         ],
         userRemoteConfigs: scm.userRemoteConfigs
    ])
    
    sh 'git log'
    echo '*** Hello ***'
}
