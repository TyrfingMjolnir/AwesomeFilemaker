Put CA inside FileMaker Pro to avoid warnings: `cp mydommain.CA.pem "/Applications/FileMaker Pro 16 Advanced/FileMaker Pro Advanced.app/Contents/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/"`

Listing of *.pem in FileMaker 16 Server
```$ exa -T /Web Publishing/publishing-engine/wip/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/```
```.
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
└── server.pem```

```$ exa -T "/Library/FileMaker Server/Web Publishing/publishing-engine/cwpc/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/"```

```.
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

./Library/Application Support/FileMaker/Shared/16.0/server.pem
./Library/Application Support/FileMaker/Shared/16.0/certifiedroot.pem
./Library/Application Support/FileMaker/Shared/16.0/root.pem
./HTTPServer/conf/server.pem
./CStore/server.pem
./CStore/certifiedroot.pem
./CStore/root.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/server.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/GeoTrust_Global_CA.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/Comodo_addtrustexternalcaroot.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/SymantecClass3PublicPrimaryG7.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/GeoTrust_Primary_CA_G2_ECC.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/entrust_ec1_ca.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/entrust_g2_ca.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/Geotrust_PCA_G3_Root.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/Symantec_PCA_2_G6.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/thawte_Timestamping_CA.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/GeoTrust_Primary_CA_G4_DSA.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/GeoTrust_Universal_CA2.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/GeoTrust_Primary_CA.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/entrust_ev_ca.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/VeriSign_Class 3 Public Primary Certification Authority.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/VeriSign Universal Root Certification Authority.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/thawte_Primary_Root_CA-G2_ECC.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/VeriSign Class 3 Public Primary Certification Authority - G3.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/COMODO High-Assurance Secure Server CA.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/VeriSign_Class 2 Public Primary Certification Authority - G2.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/COMODORSAAddTrustCA.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/GoDaddy_gd-class2-root.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/entrust_2048_ca.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/entrust_g3_ca.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/Comodo_rsacertificationauthority.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/VeriSign Class 3 Public Primary Certification Authority - G5.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/VeriSign_Class 1 Public Primary Certification Authority.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/VeriSign_Class 3 Public Primary Certification Authority - G2.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/VeriSign Class 3 Public Primary Certification Authority - G4.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/VeriSign Class 2 Public Primary Certification Authority - G3.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/thawte_Primary_Root_CA-G4_DSA.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/VeriSign_Class 2 Public Primary Certification Authority.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/GeoTrust_Global_CA2.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/VeriSign Class 1 Public Primary Certification Authority - G3.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/VeriSign_Class 4 Public Primary Certification Authority - G2.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/GeoTrust_Universal_CA.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/GoDaddy_gdroot-g3.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/thawte_Primary_Root_CA.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/GoDaddy_gdroot-g2.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/COMODORSAOrganizationValidationSecureServerCA.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/COMODO EssentialSSL CA.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/Symantec_PCA_1_G6.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/VeriSign Class 4 Public Primary Certification Authority - G3.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/VeriSign_Class 1 Public Primary Certification Authority - G2.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/GoDaddy_gdroot-g4.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/RootCA/thawte_Primary_Root_CA-G3_SHA256.pem
./Database Server/Frameworks/Support.framework/Versions/A/Resources/OpenSSL/root.pem
```
