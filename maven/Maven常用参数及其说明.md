* -h, --help              Display help infomation  
* -am, --also-make        构建指定模块，同时构建指定模块依赖的其他模块  
* -amd, --also-make-dependents       构建指定模块，同时构建依赖于指定模块的其他模块  
* -B, batch-mode          以批处理模式(batch)运行  
* -C, --strick-checksums  检查不通过，则构建失败，（严格检查）  
* -c, --lax-checksums     检查不通过，则警告（宽松检查）  
* -D, --define<arg>       Define a system property  
* -e, --errors            显示详细的错误信息  
* -emp, --encrypt-password<args>        Encrypt master security password  
* -ep, --encrypt-password<args>         Encrypt server password  
* -f, --file<args>        使用指定的POM文件替代当前POM文件  
* -fae, --fail-at-end     最后失败模式：maven会在构建最后失败（停止）。如果Maven refactor中一个失败了，Maven会继续构建其他项目，并在构建最后报告失败。  
* -ff, --fail-fast        最快失败模式：多模块构建时，遇到第一个失败的构建时停止    
* -fn, --fail-never       从不失败模式：Maven从来不会为一个失败停止，也不会报告失败  
* -gs, --global-setting<args>           替换全局级别settings.xml文件（Alternate path for the global settings file）  
* -L, --Log-file<arg>     指定输出日志文件  
* -N, --non-recursive     仅构建当前模块，而不构建子模块  
* -nsu, --no-snapshot-updates           强制不更新SNAPSHOT（Suppress SNAPSHOT updates）  
* -U, --update-snapshots                强制更新release，snapshot类型的插件或者依赖库  
* -o, --offLine           运行offline模式，不联网进行依赖更新  
* -P, --activate-profiles<arg>          激活指定的profile文件列表（用逗号[,]隔开）  
* -pL, --projects<arg>    手动选择需要构建的项目，项目间以逗号分隔，A project can be specified by [groupId]:artifactId or by its relative path.  
* -q, --quiet             安静模式，只输出ERROR  
* -rf, --resume-from<arg>               从指定的项目(或模块)开始继续构建  
* -s, --settings<arg>     替换用户级别setting.xml文件(Alternate path for the user settings file)  
* -T, --threads<arg>      Thread count, for instance 2.0C where C is core multiplied  
* -t, --toolchains<arg>   Alternate path for the user toolchains file  
* -V, --show-version      Display version information WITHOUT stopping build  
* -v, -- version          Display version information  
* -X, --debug             输出详细信息，debug模式  
* -cpu, --check-plugin-updates          【废弃】，仅为了向后兼容
* -npr, --no-plugin-registry            【废弃】，仅为了向后兼容
* -npu, --no-plugin-updates             【废弃】，仅为了向后兼容
* -up, --update-plugins                 【废弃】，仅为了向后兼容
  
- 必选的Profile一遍配置在settings.xml中，始终激活；
- 可选的Profile一般配置在pom.xml中，持续集成时，根据不同环境激活不同的Profile；
- $mvn help:active-profiles 列出当前激活的Profile
- $mvn help:all-profiles 列出当前所有的Profile
