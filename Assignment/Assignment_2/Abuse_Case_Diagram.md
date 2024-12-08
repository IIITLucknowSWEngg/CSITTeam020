![usecasediagram](https://www.planttext.com/api/plantuml/png/VLLDRzim3BqRy7yGSjeEmVx1q3HjqGBjaiqhi1rLcusrs9OXqUswNpzH_g9ajvSWV7oqgCT7-yAYDDZLLPgaIGNFA50BequbYa8Po57fXbAei09n-7qGUrstu49jn5RidZeBOY_TpvMI9oDh8ikSiZj4cP_1ZF6DaLtHLT3WemKZf1MR6HA4RKRgWwnKhdHdRxL5pvmGGT14lDJu3V1LcxDdkL0CyOOQSStbrDic-tulxfe__Nqsn7N8133YtcXhjvb245bkL8kgEObFlxBiiwzoVnZvM2fREe9FZG7BNqcKujA0p4jI0-eMFPNm7WvEXi89eMGbib8QEjUhwolcv91ZXJVo34u8VNQmzMn2He2tAzzgajghtlVS8nvWnCT6TbXge_v18Ov6js3mpGi_NfOp1fmVD9OSNi0yzOtuCXR75_W1BmfUxPVhvYHFG5rDLvaXLhJhKDSINOE-_CCoPmkkWnkiR4dVgSy7G5cueVJE6D8Zo6Ua6_GALbeNuwK6SCHuZySxSVsthRH2EHdFWHnZzCcFGZ_FA-2UN_Gcc2120dl_D9tRatjdNK_q8KMCulI5feEPD00HpLkMLjpeMWtc8so6wE1njSLs-pNQf23broL0vYq9OBuHQHAzAOYmiW0hhD3uAuJGyEyyWVijJTWhPadedHLHbWQA20l7f4dunYFIweejQS5ABTFnVPQCK98quUFq1EOcDyyOcYSt3JBqoc9odXUuZuzjcUKDBhChCYr9JAIu_r2WZxCqxPWH3tjLXMZdtr7g0fh2Vud_0m00)

@startuml

left to right direction

title OYO Competitor - Abuse Case Diagram

actor Attacker

actor FraudulentUser as "Fraudulent User"

actor MaliciousHost as "Malicious Host"

actor BotNetwork as "Bot Network"

usecase "SQL Injection" as SQLInjection

usecase "Cross-Site Scripting (XSS)" as XSS

usecase "Phishing" as Phishing

usecase "Data Breach Attempt" as DataBreach

usecase "Credential Sharing Abuse" as CredentialSharing

usecase "Fake Bookings" as FakeBookings

usecase "Payment Fraud" as PaymentFraud

usecase "Unauthorized Property Hosting" as UnauthorizedHosting

usecase "Property Overbooking" as Overbooking

usecase "Fake Reviews/Engagement" as FakeEngagement

usecase "Automated Fake Engagement" as FakeEngagementBots

usecase "Scraping Property Metadata" as ScrapingMetadata

usecase "Content Flooding" as ContentFlooding

usecase "API Exploitation" as APIExploitation

usecase "Injection of Malicious Code" as MaliciousCode

usecase "Trust Loss" as TrustLoss

usecase "Revenue Loss" as RevenueLoss

usecase "Data Compromise" as DataCompromise

Attacker --> SQLInjection

Attacker --> XSS

Attacker --> Phishing

Attacker --> DataBreach

FraudulentUser --> CredentialSharing

FraudulentUser --> FakeBookings

FraudulentUser --> PaymentFraud

FraudulentUser --> FakeEngagement

BotNetwork --> FakeEngagementBots

BotNetwork --> ScrapingMetadata

BotNetwork --> ContentFlooding

MaliciousHost --> UnauthorizedHosting

MaliciousHost --> Overbooking

MaliciousHost --> FakeEngagement

MaliciousHost --> PaymentFraud

SQLInjection --> TrustLoss

XSS --> TrustLoss

DataBreach --> DataCompromise

CredentialSharing --> RevenueLoss

FakeBookings --> RevenueLoss

PaymentFraud --> RevenueLoss

UnauthorizedHosting --> RevenueLoss

Overbooking --> TrustLoss

FakeEngagement --> TrustLoss

FakeEngagementBots --> TrustLoss

ScrapingMetadata --> DataCompromise

APIExploitation --> DataCompromise

@enduml
