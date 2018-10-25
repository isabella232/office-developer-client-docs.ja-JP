---
title: Outlook で使用される名前付きプロパティについて
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8c245ec2-bb18-ecf0-b4ad-8c164c5924cf
description: '最終更新日: 2012 年 6 月 25 日'
ms.openlocfilehash: aa4d52d25f120e8b3e2a4c0dcaa4845ad576127a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566230"
---
# <a name="about-named-properties-used-by-outlook"></a>Outlook で使用される名前付きプロパティについて

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI は、特定のプロパティに名前を割り当て、これらの名前を一意識別子にマッピングし、この名前から識別子へのマッピングをセッション間で永続化するための機能を提供します。名前付きプロパティは、プロパティ セットの名前とグローバル一意識別子 (GUID) によって識別されます。名前には、数値または文字列を使用することができます。Microsoft Outlook 2013 または Microsoft Outlook 2010 のプロパティ セットの多くは、**PSETID_Appointment** などの、Outlook 2013 または Outlook 2010 で定義された名前空間です。 
  
名前付きプロパティは、[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) 関数や [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) 関数を使って操作されます。名前とプロパティ セット GUID は [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) 関数に回されて、現在の MAPI セッションに有効なプロパティ識別子を取得します。プロパティ識別子はコンピューター端末によって異なることがあるため、名前付きのプロパティに一貫してアクセスする唯一の方法は、そのプロパティの名前とプロパティ セット GUID を知ることです。識別子の範囲は常に 0x8000 から 0xFFFE の間です。 
  
[IMAPIProp : IUnknown](imapipropiunknown.md) インターフェイスを実装するオブジェクトはすべて、名前付きプロパティをサポートすることができます。具体的には、MAPI サービス プロバイダーまたは MAPI クライアントは [IMAPIProp::GetProps](imapiprop-getprops.md) を実装して、名前付きプロパティの値を取得する必要があります。Outlook 2013 または Outlook 2010 で使用される名前付きプロパティの設定はサポートされていません。これは、他の MAPI プロバイダーまたはクライアントと共有されるデータが破損する危険があるためです。 
  
Outlook 2013 と Outlook 2010 では、MAPI の名前付きプロパティを使用して、添付ファイルのセキュリティや会議の代替日時の提案などのさまざまな機能を実装しています。 Outlook 2013 と Outlook 2010 は、この基盤となるデータ上で、Outlook 2013 と Outlook 2010 のオブジェクト モデルのアイテム プロパティとして、これらのプロパティの一部を公開しています。 たとえば、オブジェクト モデル内の **ContactItem** オブジェクトである **Email1Address** プロパティは、**PSETID_Address** 名前空間にある名前付きの [PidLidEmail1EmailAddress 標準プロパティ](pidlidemail1emailaddress-canonical-property.md)に対応します。 しかし、一般に、互換性とデータの整合性に対する懸念から、Outlook 2013 と Outlook 2010 で使用される MAPI プロパティの多くはオブジェクト モデルに公開されていません。 
  
このリファレンスでは、以下に列挙する多数の名前付きプロパティについて説明します。
  
**PSETID_Address** 名前空間の名前付きプロパティは、次のとおりです。 
  
- [PidLidEmail1AddressType 標準プロパティ](pidlidemail1addresstype-canonical-property.md)
    
- [PidLidEmail1EmailAddress 標準プロパティ](pidlidemail1emailaddress-canonical-property.md)
    
- [PidLidEmail1OriginalEntryId 標準プロパティ](pidlidemail1originalentryid-canonical-property.md)
    
- [PidLidEmail2AddressType 標準プロパティ](pidlidemail2addresstype-canonical-property.md)
    
- [PidLidEmail2DisplayName 標準プロパティ](pidlidemail2displayname-canonical-property.md)
    
- [PidLidEmail2EmailAddress 標準プロパティ](pidlidemail2emailaddress-canonical-property.md)
    
- [PidLidEmail2OriginalDisplayName 標準プロパティ](pidlidemail2originaldisplayname-canonical-property.md)
    
- [PidLidEmail2OriginalEntryId 標準プロパティ](pidlidemail2originalentryid-canonical-property.md)
    
- [PidLidEmail3AddressType 標準プロパティ](pidlidemail3addresstype-canonical-property.md)
    
- [PidLidEmail3DisplayName 標準プロパティ](pidlidemail3displayname-canonical-property.md)
    
- [PidLidEmail3EmailAddress 標準プロパティ](pidlidemail3emailaddress-canonical-property.md)
    
- [PidLidEmail3OriginalDisplayName 標準プロパティ](pidlidemail3originaldisplayname-canonical-property.md)
    
- [PidLidEmail3OriginalEntryId 標準プロパティ](pidlidemail3originalentryid-canonical-property.md)
    
- [PidLidEmail1DisplayName 標準プロパティ](pidlidemail1displayname-canonical-property.md)
    
- [PidLidEmail1OriginalDisplayName 標準プロパティ](pidlidemail1originaldisplayname-canonical-property.md)
    
- [PidLidFileUnder 標準プロパティ](pidlidfileunder-canonical-property.md)
    
- [PidLidInstantMessagingAddress 標準プロパティ](pidlidinstantmessagingaddress-canonical-property.md)
    
- [PidLidWorkAddressCity 標準プロパティ](pidlidworkaddresscity-canonical-property.md)
    
- [PidLidWorkAddressCountry 標準プロパティ](pidlidworkaddresscountry-canonical-property.md)
    
- [PidLidWorkAddressPostalCode 標準プロパティ](pidlidworkaddresspostalcode-canonical-property.md)
    
- [PidLidWorkAddressPostOfficeBox 標準プロパティ](pidlidworkaddresspostofficebox-canonical-property.md)
    
- [PidLidWorkAddressState 標準プロパティ](pidlidworkaddressstate-canonical-property.md)
    
- [PidLidWorkAddressStreet 標準プロパティ](pidlidworkaddressstreet-canonical-property.md)
    
- [PidLidYomiCompanyName 標準プロパティ](pidlidyomicompanyname-canonical-property.md)
    
- [PidLidYomiFirstName 標準プロパティ](pidlidyomifirstname-canonical-property.md)
    
- [PidLidYomiLastName 標準プロパティ](pidlidyomilastname-canonical-property.md)
    
**PSETID_Appointment** 名前空間の名前付きプロパティは、次のとおりです。 
  
- [PidLidAllAttendeesString 標準プロパティ](pidlidallattendeesstring-canonical-property.md)
    
- [PidLidAppointmentCounterProposal 標準プロパティ](pidlidappointmentcounterproposal-canonical-property.md)
    
- [PidLidAppointmentDuration 標準プロパティ](pidlidappointmentduration-canonical-property.md)
    
- [PidLidAppointmentEndWhole 標準プロパティ](pidlidappointmentendwhole-canonical-property.md)
    
- [PidLidAppointmentStartWhole 標準プロパティ](pidlidappointmentstartwhole-canonical-property.md)
    
- [PidLidBusyStatus 標準プロパティ](pidlidbusystatus-canonical-property.md)
    
- [PidLidCcAttendeesString 標準プロパティ](pidlidccattendeesstring-canonical-property.md)
    
- [PidLidLocation 標準プロパティ](pidlidlocation-canonical-property.md)
    
- [PidLidRecurring 標準プロパティ](pidlidrecurring-canonical-property.md)
    
- [PidLidToAttendeesString 標準プロパティ](pidlidtoattendeesstring-canonical-property.md)
    
**PSETID_Common** 名前空間の名前付きプロパティは、次のとおりです。 
  
- [PidLidCommonEnd 標準プロパティ](pidlidcommonend-canonical-property.md)
    
- [PidLidCommonStart 標準プロパティ](pidlidcommonstart-canonical-property.md)
    
- [PidLidCompanies 標準プロパティ](pidlidcompanies-canonical-property.md)
    
- [PidLidContacts 標準プロパティ](pidlidcontacts-canonical-property.md)
    
- [PidLidCustomFlag 標準プロパティ](pidlidcustomflag-canonical-property.md)
    
- [PidLidFormPropStream 標準プロパティ](pidlidformpropstream-canonical-property.md)
    
- [PidLidFormStorage 標準プロパティ](pidlidformstorage-canonical-property.md)
    
- [PidLidHeaderItem 標準プロパティ](pidlidheaderitem-canonical-property.md)
    
- [PidLidPageDirStream 標準プロパティ](pidlidpagedirstream-canonical-property.md)
    
- [PidLidPropertyDefinitionStream 標準プロパティ](pidlidpropertydefinitionstream-canonical-property.md)
    
- [PidLidReminderSet 標準プロパティ](pidlidreminderset-canonical-property.md)
    
- [PidLidReminderTime 標準プロパティ](pidlidremindertime-canonical-property.md)
    
- [PidLidFlagRequest 標準プロパティ](pidlidflagrequest-canonical-property.md)
    
- [PidLidScriptStream 標準プロパティ](pidlidscriptstream-canonical-property.md)
    
- [PidLidSmartNoAttach 標準プロパティ](pidlidsmartnoattach-canonical-property.md)
    
- [PidLidToDoTitle 標準プロパティ](pidlidtodotitle-canonical-property.md)
    
- [PidLidUseTnef 標準プロパティ](pidlidusetnef-canonical-property.md)
    
**PSETID_Meeting** 名前空間の名前付きプロパティは、次のとおりです。 
  
- [PidLidMeetingType 標準プロパティ](pidlidmeetingtype-canonical-property.md)
    
**PSETID_Task** 名前空間の名前付きプロパティは、次のとおりです。 
  
- [PidLidTaskActualEffort 標準プロパティ](pidlidtaskactualeffort-canonical-property.md)
    
- [PidLidTaskDueDate 標準プロパティ](pidlidtaskduedate-canonical-property.md)
    
- [PidLidTaskEstimatedEffort 標準プロパティ](pidlidtaskestimatedeffort-canonical-property.md)
    
- [PidLidTaskFRecurring 標準プロパティ](pidlidtaskfrecurring-canonical-property.md)
    
- [PidLidTaskStartDate 標準プロパティ](pidlidtaskstartdate-canonical-property.md)
    
- [PidLidTaskStatus 標準プロパティ](pidlidtaskstatus-canonical-property.md)
    
**PS_INTERNET_HEADERS** 名前空間の名前付きプロパティは、次のとおりです。 
  
- [PidTagInternetReturnPath 標準プロパティ](pidtaginternetreturnpath-canonical-property.md)
    
**PSETID_Log** 名前空間の名前付きプロパティは、次のとおりです。 
  
- [PidLidLogDuration 標準プロパティ](pidlidlogduration-canonical-property.md)
    
- [PidLidLogEnd 標準プロパティ](pidlidlogend-canonical-property.md)
    
- [PidLidLogStart 標準プロパティ](pidlidlogstart-canonical-property.md)
    
- [PidLidLogType 標準プロパティ](pidlidlogtype-canonical-property.md)
    
**PS_PUBLIC_STRINGS** 名前空間の名前付きプロパティは、次のとおりです。 
  
- [PidNameKeywords 標準プロパティ](pidnamekeywords-canonical-property.md)
    
- [PidNameExchangeJunkEmailMoveStamp 標準プロパティ](pidnameexchangejunkemailmovestamp-canonical-property.md)
    
## <a name="see-also"></a>関連項目



[MAPI 定数](mapi-constants.md)
  
[Outlook がメッセージのヘッダーのみをダウンロードしたかどうかを判別する](how-to-determine-if-outlook-downloaded-only-the-header-of-a-message.md)
  
[連絡先アイテムのメール アドレスを取得する](how-to-get-the-email-address-of-a-contact-item.md)
  
[メッセージと共に保存されているユーザー設定フォーム定義を削除する](how-to-remove-custom-form-definition-saved-with-a-message.md)

