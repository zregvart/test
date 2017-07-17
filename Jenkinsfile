node {
    checkout([
         $class: 'GitSCM',
         branches: scm.branches,
         doGenerateSubmoduleConfigurations: scm.doGenerateSubmoduleConfigurations,
         extensions: scm.extensions + [[
             $class: 'PreBuildMerge',
             options: [
                 fastForwardMode: 'FF',
                 mergeTarget: 'master'
             ]
         ]],
         userRemoteConfigs: scm.userRemoteConfigs
    ])
}
