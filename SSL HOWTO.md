# HOW-TO self sign SSL Certificate for FileMaker 16 Server
may also work with other versions.

## Practical information

1. Make sure you have a new dedicated removable device such as SD card or USB MASS Storage device handy
1. Make sure you grab a HOW-TO( I use FireFox and push CMD + S )
1. Disconnect your computer from the internet
1. Sign the certificates: CA, domain, host[s] on the removable
1. Copy the public files to your computer
1. Unmount the removable
1. Put the removable in a safe
1. reconnect your computer to the internet

### Prior art
This blog is a very valuable lesson if you appreciate security; while a publicly signed SSL certificate can be good circumstancial reference to who is serving the data, not unlike car number plates. Self signed certificates are a hope of providing actual security for your data transfer: https://blog.beezwax.net/2017/12/03/creating-your-own-ssl-certificates-for-filemaker/ That said I was never able to follow that guide using the GUI to create a self signed certificate; hence I used openssl to sign the certificates myself. Also that blog does not tell you some of the most important steps of creating a self signed certificate such as signing to an SD card while the computer is offline, and only copying the public files to your computer, disconnecting the SD card and storing that SD card in a physical fire proof safe.

### Convenience function for self signed certificate
After self signing your certificates putting the CA in each your trusted clients as read only may be a nice convenience for your users: How to put CA inside FileMaker Pro to avoid warnings: `cp mydommain.CA.pem "/Applications/FileMaker Pro 16 Advanced/FileMaker Pro Advanced.app/Contents/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/"`

### Below are listings of *.pem-files in FileMaker 16 Server installation on MacOD X Mojave
```
$ exa -T /Web Publishing/publishing-engine/wip/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/
```

```
OpenSSL
├── keypairstore.xml
├── openssl.config
├── root.pem
├── RootCA
│  ├── Comodo_addtrustexternalcaroot.pem
│  ├── Comodo_rsacertificationauthority.pem
│  ├── COMODO EssentialSSL CA.pem
│  ├── COMODO High-Assurance Secure Server CA.pem
│  ├── COMODORSAAddTrustCA.pem
│  ├── COMODORSAOrganizationValidationSecureServerCA.pem
│  ├── entrust_2048_ca.pem
│  ├── entrust_ec1_ca.pem
│  ├── entrust_ev_ca.pem
│  ├── entrust_g2_ca.pem
│  ├── entrust_g3_ca.pem
│  ├── GeoTrust_Global_CA.pem
│  ├── GeoTrust_Global_CA2.pem
│  ├── Geotrust_PCA_G3_Root.pem
│  ├── GeoTrust_Primary_CA.pem
│  ├── GeoTrust_Primary_CA_G2_ECC.pem
│  ├── GeoTrust_Primary_CA_G4_DSA.pem
│  ├── GeoTrust_Universal_CA.pem
│  ├── GeoTrust_Universal_CA2.pem
│  ├── GoDaddy_gd-class2-root.pem
│  ├── GoDaddy_gdroot-g2.pem
│  ├── GoDaddy_gdroot-g3.pem
│  ├── GoDaddy_gdroot-g4.pem
│  ├── Symantec_PCA_1_G6.pem
│  ├── Symantec_PCA_2_G6.pem
│  ├── SymantecClass3PublicPrimaryG7.pem
│  ├── thawte_Primary_Root_CA-G2_ECC.pem
│  ├── thawte_Primary_Root_CA-G3_SHA256.pem
│  ├── thawte_Primary_Root_CA-G4_DSA.pem
│  ├── thawte_Primary_Root_CA.pem
│  ├── thawte_Timestamping_CA.pem
│  ├── VeriSign_Class 1 Public Primary Certification Authority - G2.pem
│  ├── VeriSign_Class 1 Public Primary Certification Authority.pem
│  ├── VeriSign_Class 2 Public Primary Certification Authority - G2.pem
│  ├── VeriSign_Class 2 Public Primary Certification Authority.pem
│  ├── VeriSign_Class 3 Public Primary Certification Authority - G2.pem
│  ├── VeriSign_Class 3 Public Primary Certification Authority.pem
│  ├── VeriSign_Class 4 Public Primary Certification Authority - G2.pem
│  ├── VeriSign Class 1 Public Primary Certification Authority - G3.pem
│  ├── VeriSign Class 2 Public Primary Certification Authority - G3.pem
│  ├── VeriSign Class 3 Public Primary Certification Authority - G3.pem
│  ├── VeriSign Class 3 Public Primary Certification Authority - G4.pem
│  ├── VeriSign Class 3 Public Primary Certification Authority - G5.pem
│  ├── VeriSign Class 4 Public Primary Certification Authority - G3.pem
│  └── VeriSign Universal Root Certification Authority.pem
└── server.pem
```

```
$ exa -T "/Library/FileMaker Server/Web Publishing/publishing-engine/cwpc/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/"
```

```
OpenSSL
├── keypairstore.xml
├── openssl.config
├── root.pem
├── RootCA
│  ├── Comodo_addtrustexternalcaroot.pem
│  ├── Comodo_rsacertificationauthority.pem
│  ├── COMODO EssentialSSL CA.pem
│  ├── COMODO High-Assurance Secure Server CA.pem
│  ├── COMODORSAAddTrustCA.pem
│  ├── COMODORSAOrganizationValidationSecureServerCA.pem
│  ├── entrust_2048_ca.pem
│  ├── entrust_ec1_ca.pem
│  ├── entrust_ev_ca.pem
│  ├── entrust_g2_ca.pem
│  ├── entrust_g3_ca.pem
│  ├── GeoTrust_Global_CA.pem
│  ├── GeoTrust_Global_CA2.pem
│  ├── Geotrust_PCA_G3_Root.pem
│  ├── GeoTrust_Primary_CA.pem
│  ├── GeoTrust_Primary_CA_G2_ECC.pem
│  ├── GeoTrust_Primary_CA_G4_DSA.pem
│  ├── GeoTrust_Universal_CA.pem
│  ├── GeoTrust_Universal_CA2.pem
│  ├── GoDaddy_gd-class2-root.pem
│  ├── GoDaddy_gdroot-g2.pem
│  ├── GoDaddy_gdroot-g3.pem
│  ├── GoDaddy_gdroot-g4.pem
│  ├── Symantec_PCA_1_G6.pem
│  ├── Symantec_PCA_2_G6.pem
│  ├── SymantecClass3PublicPrimaryG7.pem
│  ├── thawte_Primary_Root_CA-G2_ECC.pem
│  ├── thawte_Primary_Root_CA-G3_SHA256.pem
│  ├── thawte_Primary_Root_CA-G4_DSA.pem
│  ├── thawte_Primary_Root_CA.pem
│  ├── thawte_Timestamping_CA.pem
│  ├── VeriSign_Class 1 Public Primary Certification Authority - G2.pem
│  ├── VeriSign_Class 1 Public Primary Certification Authority.pem
│  ├── VeriSign_Class 2 Public Primary Certification Authority - G2.pem
│  ├── VeriSign_Class 2 Public Primary Certification Authority.pem
│  ├── VeriSign_Class 3 Public Primary Certification Authority - G2.pem
│  ├── VeriSign_Class 3 Public Primary Certification Authority.pem
│  ├── VeriSign_Class 4 Public Primary Certification Authority - G2.pem
│  ├── VeriSign Class 1 Public Primary Certification Authority - G3.pem
│  ├── VeriSign Class 2 Public Primary Certification Authority - G3.pem
│  ├── VeriSign Class 3 Public Primary Certification Authority - G3.pem
│  ├── VeriSign Class 3 Public Primary Certification Authority - G4.pem
│  ├── VeriSign Class 3 Public Primary Certification Authority - G5.pem
│  ├── VeriSign Class 4 Public Primary Certification Authority - G3.pem
│  └── VeriSign Universal Root Certification Authority.pem
└── server.pem
```

```
sudo exa -T "/Library/FileMaker Server/Library/"
```

```
Library
├── Application Support
│  └── FileMaker
│     └── Shared
│        └── 16.0
│           ├── certifiedroot.pem
│           ├── root.pem
│           └── server.pem
├── Keychains
│  └── 86676CA6-E0F5-5E28-AF8E-7CB437FC2785
│     ├── Analytics
│     │  ├── ckks_analytics.db
│     │  ├── ckks_analytics.db-shm
│     │  ├── ckks_analytics.db-wal
│     │  ├── sos_analytics.db
│     │  ├── sos_analytics.db-shm
│     │  └── sos_analytics.db-wal
│     ├── keychain-2.db
│     ├── keychain-2.db-shm
│     └── keychain-2.db-wal
├── Preferences
│  ├── com.apple.LaunchServices
│  └── com.apple.security.cloudkeychainproxy3.keysToRegister.plist
└── SyncedPreferences
   └── com.apple.syncedpreferences.plist
```

```
exa -T "/Library/FileMaker Server/HTTPServer/"
```

```
HTTPServer
└── conf
   └── server.pem
```

```
exa -T "/Library/FileMaker Server/CStore/"
```

```
CStore
├── certifiedroot.pem
├── fmcacerts
├── keystore
├── machinePublicKey
├── root.pem
├── server.pem
└── uninstall.sh
```

```
$ exa -T "/Library/FileMaker Server/Database\ Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/"
```

```
OpenSSL
├── keypairstore.xml
├── openssl.config
├── root.pem
├── RootCA
│  ├── Comodo_addtrustexternalcaroot.pem
│  ├── Comodo_rsacertificationauthority.pem
│  ├── COMODO EssentialSSL CA.pem
│  ├── COMODO High-Assurance Secure Server CA.pem
│  ├── COMODORSAAddTrustCA.pem
│  ├── COMODORSAOrganizationValidationSecureServerCA.pem
│  ├── entrust_2048_ca.pem
│  ├── entrust_ec1_ca.pem
│  ├── entrust_ev_ca.pem
│  ├── entrust_g2_ca.pem
│  ├── entrust_g3_ca.pem
│  ├── GeoTrust_Global_CA.pem
│  ├── GeoTrust_Global_CA2.pem
│  ├── Geotrust_PCA_G3_Root.pem
│  ├── GeoTrust_Primary_CA.pem
│  ├── GeoTrust_Primary_CA_G2_ECC.pem
│  ├── GeoTrust_Primary_CA_G4_DSA.pem
│  ├── GeoTrust_Universal_CA.pem
│  ├── GeoTrust_Universal_CA2.pem
│  ├── GoDaddy_gd-class2-root.pem
│  ├── GoDaddy_gdroot-g2.pem
│  ├── GoDaddy_gdroot-g3.pem
│  ├── GoDaddy_gdroot-g4.pem
│  ├── Symantec_PCA_1_G6.pem
│  ├── Symantec_PCA_2_G6.pem
│  ├── SymantecClass3PublicPrimaryG7.pem
│  ├── thawte_Primary_Root_CA-G2_ECC.pem
│  ├── thawte_Primary_Root_CA-G3_SHA256.pem
│  ├── thawte_Primary_Root_CA-G4_DSA.pem
│  ├── thawte_Primary_Root_CA.pem
│  ├── thawte_Timestamping_CA.pem
│  ├── VeriSign_Class 1 Public Primary Certification Authority - G2.pem
│  ├── VeriSign_Class 1 Public Primary Certification Authority.pem
│  ├── VeriSign_Class 2 Public Primary Certification Authority - G2.pem
│  ├── VeriSign_Class 2 Public Primary Certification Authority.pem
│  ├── VeriSign_Class 3 Public Primary Certification Authority - G2.pem
│  ├── VeriSign_Class 3 Public Primary Certification Authority.pem
│  ├── VeriSign_Class 4 Public Primary Certification Authority - G2.pem
│  ├── VeriSign Class 1 Public Primary Certification Authority - G3.pem
│  ├── VeriSign Class 2 Public Primary Certification Authority - G3.pem
│  ├── VeriSign Class 3 Public Primary Certification Authority - G3.pem
│  ├── VeriSign Class 3 Public Primary Certification Authority - G4.pem
│  ├── VeriSign Class 3 Public Primary Certification Authority - G5.pem
│  ├── VeriSign Class 4 Public Primary Certification Authority - G3.pem
│  └── VeriSign Universal Root Certification Authority.pem
└── server.pem
```
