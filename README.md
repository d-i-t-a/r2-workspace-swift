# r2-workspace-swift
A workspace for on-boarding developers

This workspace is one of the ways you can get started with the R2 Swift Projects. It is not the only way and you can pick to setup your development environment in the way that best fits your needs.

### Prerequisite
- install/update [Carthage](https://github.com/Carthage/Carthage)
- install/update [Carting](https://github.com/artemnovichkov/Carting) 
- Xcode 10.x
- Swift 4.2



In this workspace you will find 4 Github branches:

### int/testapp
You pick this branch if are an integrator and all you need is to quickly get started with the R2 Testapp. 

1. git clone --recurse-submodules -b int/testapp https://github.com/readium/r2-workspace-swift.git
2. ckeckout **int/testapp** branch **including it's submodules**
3. run **carthage update --platform ios** on r2-testapp-swift
8. run **carting update** on r2-testapp-swift
4. open **r2-workspace-swift.xcworkspace**
5. run target **r2-testapp-swift (carthage)**

**Cartfile should look like this:**

```
github "readium/r2-shared-swift" "develop"
github "readium/r2-streamer-swift" "develop"
github "readium/r2-navigator-swift" "develop"
github "readium/readium-opds-swift" "develop"
github "edrlab/ZIPFoundation" "master"
github "onevcat/Kingfisher" == 4.6.4
github "jdg/MBProgressHUD" ~> 1.1.0
github "stephencelis/SQLite.swift" == 0.11.5
github "tadija/AEXML" == 4.3.3
github "swisspol/GCDWebServer" == 3.5.2
github "krzyzanowskim/CryptoSwift" == 0.14.0
github "cezheng/Fuzi" == 2.1.0
github "dexman/Minizip"
```

### dev/testapp
You pick this branch if are an developer and a R2 contributor. You can get started quickly on the R2 Testapp and it's modules with this branch. We do appreciate any contribution, no matter how small it is, it makes a difference :) 

1. git clone --recurse-submodules -b dev/testapp https://github.com/readium/r2-workspace-swift.git
2. ckeckout **dev/testapp** branch **including it's submodules**
7. run **carthage update --platform ios** on r2-testapp-swift
8. run **carting update** on r2-testapp-swift
8. open **r2-workspace-swift.xcworkspace**
9. run target **r2-testapp-swift (submodules)**

**Cartfile should look like this:**

```
github "edrlab/ZIPFoundation" "master"
github "onevcat/Kingfisher" == 4.6.4
github "jdg/MBProgressHUD" ~> 1.1.0
github "stephencelis/SQLite.swift" == 0.11.5
github "tadija/AEXML" == 4.3.3
github "swisspol/GCDWebServer" == 3.5.2
github "krzyzanowskim/CryptoSwift" == 0.14.0
github "cezheng/Fuzi" == 2.1.0
github "dexman/Minizip"
```

### int/testapp-with-lcp
You pick this branch if are an integrator and you would like to get started with the R2 Testapp supporting LCP. 

1. git clone --recurse-submodules -b int/testapp-with-lcp  https://github.com/readium/r2-workspace-swift.git
2. ckeckout **int/testapp-with-lcp** branch **including it's submodules**
3. run **carthage update --platform ios** on r2-testapp-swift
8. run **carting update** on r2-testapp-swift
4. copy **liblcp.a** to the root of **r2-lcp-wrapper-swift** directory
5. open **r2-workspace-swift.xcworkspace**
6. run target **r2-testapp-swift (carthage-with-lcp)**

**Cartfile should look like this:**

```
github "readium/r2-shared-swift" "develop"
github "readium/r2-streamer-swift" "develop"
github "readium/r2-navigator-swift" "develop"
github "readium/readium-opds-swift" "develop"
github "edrlab/ZIPFoundation" "master"
github "onevcat/Kingfisher" == 4.6.4
github "jdg/MBProgressHUD" ~> 1.1.0
github "stephencelis/SQLite.swift" == 0.11.5
github "tadija/AEXML" == 4.3.3
github "swisspol/GCDWebServer" == 3.5.2
github "krzyzanowskim/CryptoSwift" == 0.14.0
github "cezheng/Fuzi" == 2.1.0
github "dexman/Minizip"
```


### dev/testapp-with-lcp
You pick this branch if are an developer and a R2 contributor. You can get started quickly on the R2 Testapp and it's modules including LCP with this branch. We do appreciate any contribution, no matter how small it is, it makes a difference :) 


1. git clone --recurse-submodules -b dev/testapp-with-lcp https://github.com/readium/r2-workspace-swift.git
2. ckeckout **dev/testapp-with-lcp** branch **including it's submodules**
3. update Cartfile (see below)
7. run **carthage update --platform ios** on r2-testapp-swift
8. run **carting update** on r2-testapp-swift
8. copy **liblcp.a** to the root of **r2-lcp-wrapper-swift** directory
8. open **r2-workspace-swift.xcworkspace**
9. run target **r2-testapp-swift (submodules-with-lcp)**

**Cartfile should look like this:**

```
github "edrlab/ZIPFoundation" "master"
github "onevcat/Kingfisher" == 4.6.4
github "jdg/MBProgressHUD" ~> 1.1.0
github "stephencelis/SQLite.swift" == 0.11.5
github "tadija/AEXML" == 4.3.3
github "swisspol/GCDWebServer" == 3.5.2
github "krzyzanowskim/CryptoSwift" == 0.14.0
github "cezheng/Fuzi" == 2.1.0
github "dexman/Minizip"
```
**Dependencies and the modules they are used in**
- [edrlab/ZIPFoundation](https://github.com/edrlab/ZIPFoundation) used in [ReadiumLCP](https://github.com/readium/r2-lcp-swift)
- [onevcat/Kingfisher](https://github.com/onevcat/Kingfisher) used in [R2 Testapp](https://github.com/readium/r2-testapp-swift)
- [jdg/MBProgressHUD](https://github.com/jdg/MBProgressHUD) used in [R2 Testapp](https://github.com/readium/r2-testapp-swift)
- [stephencelis/SQLite.swift](https://github.com/stephencelis/SQLite.swift) used in [R2 Testapp](https://github.com/readium/r2-testapp-swift), [ReadiumLCP](https://github.com/readium/r2-lcp-swift)
- [tadija/AEXML](https://github.com/tadija/AEXML) used in [R2Streamer](https://github.com/readium/r2-streamer-swift)
- [swisspol/GCDWebServer](https://github.com/swisspol/GCDWebServer) used in [R2Streamer](https://github.com/readium/r2-streamer-swift)
- [krzyzanowskim/CryptoSwift](https://github.com/krzyzanowskim/CryptoSwift) used in [ReadiumLCP](https://github.com/readium/r2-lcp-swift), [R2Streamer](/readium/r2-streamer-swift)
- [cezheng/Fuzi](https://github.com/cezheng/Fuzi) used in [ReadiumOPDS](https://github.com/readium/r2-opds-swift), [R2Streamer](https://github.com/readium/r2-streamer-swift)
- [dexman/Minizip](https://github.com/dexman/Minizip) used in [R2Streamer](https://github.com/readium/r2-streamer-swift)



## Getting the pre-compiled Readium LCP module.

Readium LCP is a DRM. As any protection technology, care must be taken to avoid disclosing too much technical information to the open world without good reasons. This is why EDRLab has chosen to provide a small pre-compiled Readium LCP module to R2 implementers, in two flavors:

1. a "test" grade LCP library, provided after a direct contact between the developer and EDRLab. To get this library, a developer must only provide to EDRLab its company name, web site and basic information about the context of the project involving Readium LCP.
2.  a "production" grade LCP library, which simply replaces the "test" library in the project after the development has been fully tested. Go get access to this production module, the client company must be trusted and the Readium LCP Terms of Used must have been signed.

To contact EDRLab, please send an email to contact(at)edrlab.org or use the Readium Slack on the "lcp" channel.

