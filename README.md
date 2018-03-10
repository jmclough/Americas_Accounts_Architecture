# Americas_Accounts_Architecture
Cluster Analysis - prioritized architectures based on wallet ratio within accounts

Notes
Included Named and Unnamed accounts with >$5K in FY 19 BIC Wallet, for categorization
This included GSP, as is relevant for Latam.

The results are stored in Hadoop in the following folder:

mktg_bana.amer_cie_accts_wallet_segment


"COUNTRY_NAME"                 
"CUBE_ID"                      
"Most_Important_CRsite"       
"SAV_account_id"               
"Named_Unnamed_Account_Ind"    
"Possible_Partner_Flag"       


"segmentation_description"     
Will have one of the following values:
0 Opp Acct      Description: < $5K in total BIC Wallet within the account. Not part of categorization - recommend exclusion
1 Opp Acct      Description: One arch encapsulates at least 75% of total wallet. Target according to the 1 arch
2 Opp Acct      Description: Two archs encapsulate the majority of wallet. Target according to 2 archs and ignore others
3 Opp Acct      Description: Three archs encapsulate the majority of wallet. Target according to 3 archs and ignore others
4 Opp Acct      Description: Four archs encapsulate the majority of wallet. Target according to 2 archs and ignore others

"cluster"       Description: cluster 1 to 15. Derived segmentation_description field already created and described           

The consumable_ fields are only populated if sufficient opportunity exists - according to segmentation_description
"consumable_collab_Next"      
"consumable_dcv_Next"          
"consumable_eng_Next"          
"consumable_other_Next"       
"consumable_security_Next"     
"consumable_wallet_sum"        

The Arch_bicwallet fields are the original fields - comparison from then to now (bic versus consumable)
"BICWallet_Total_Prod_Next"   
"Arch_bicwallet_collab_Next"   
"Arch_bicwallet_dcv_Next"      
"Arch_bicwallet_eng_Next"     
"Arch_bicwallet_other_Next"    
"Arch_bicwallet_security_Next"
