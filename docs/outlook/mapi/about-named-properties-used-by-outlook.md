---
title: "Outlook �Ŏg�p���閼�O�t���̃v���p�e�B�ɂ\x82���"
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 8c245ec2-bb18-ecf0-b4ad-8c164c5924cf
description: '最終更新日: 2012 年 6 月 25 日'
ms.openlocfilehash: a41f564094bd274dd1c1558700a0773ece0b0762
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551920"
---
# <a name="about-named-properties-used-by-outlook"></a>Outlook で使用される名前付きプロパティについて

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI は、特定のプロパティに名前を割り当て、これらの名前を一意識別子にマッピングし、この名前から識別子へのマッピングをセッション間で永続化するための機能を提供します。名前付きプロパティは、プロパティ セットの名前とグローバル一意識別子 (GUID) によって識別されます。名前には、数値または文字列を使用することができます。Microsoft Outlook 2013 または Microsoft Outlook 2010 のプロパティ セットの多くは、**PSETID_Appointment** などの、Outlook 2013 または Outlook 2010 で定義された名前空間です。 
  
���O�t���̃v���p�e�B�𑀍삷��ɂ́A [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)�֐���[IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)�֐���g�p���܂��B���O�� GUID �v���p�e�B�̐ݒ�́A���݂� MAPI �Z�b�V�����͗L���ȃv���p�e�B���ʎq��擾����[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)�֐��ɓn����܂��B���̃v���p�e�B�̎��ʎq���R���s���[�^�[����ʂ̃R���s���[�^�[�ɈقȂ邱�Ƃ��ł��܂��݈̂�ѐ��̂��閼�O�t���̃v���p�e�B�ɃA�N�Z�X������@�ł́A���̖��O�� GUID �v���p�e�B���킩���Ă��܂��B ���ʎq�͈̔͂́A��� 0x8000 �� 0 xfffe �͈́B 
  
[IMAPIProp : IUnknown](imapipropiunknown.md) インターフェイスを実装するオブジェクトはすべて、名前付きプロパティをサポートすることができます。具体的には、MAPI サービス プロバイダーまたは MAPI クライアントは [IMAPIProp::GetProps](imapiprop-getprops.md) を実装して、名前付きプロパティの値を取得する必要があります。Outlook 2013 または Outlook 2010 で使用される名前付きプロパティの設定はサポートされていません。これは、他の MAPI プロバイダーまたはクライアントと共有されるデータが破損する危険があるためです。 
  
Outlook 2013 and Outlook 2010 use MAPI named properties to implement many of their features, for example, attachment security and meeting counter-proposals. Above this underlying data, Outlook 2013 and Outlook 2010 expose some of these properties as item properties in their Outlook 2013 and Outlook 2010 object models. For example, the **Email1Address** property of the **ContactItem** object in the object model corresponds to the named [PidLidEmail1EmailAddress Canonical Property](pidlidemail1emailaddress-canonical-property.md) in the **PSETID_Address** namespace. But in general, due to concerns for compatibility and data integrity, many of the MAPI properties that are used by Outlook 2013 and Outlook 2010 are not exposed in the object model. 
  
���̃Z���Q�Ƃł́A�����̉��ɋL�ڂ���Ă��閼�O�t���̃v���p�e�B�ɂ��Đ�����܂��B
  
**PSETID_Address** ���O��Ԃ̃v���p�e�B�A���̂Ƃ���ł��B 
  
- [PidLidEmail1AddressType ���K���̃v���p�e�B](pidlidemail1addresstype-canonical-property.md)
    
- [PidLidEmail1EmailAddress ���K���̃v���p�e�B](pidlidemail1emailaddress-canonical-property.md)
    
- [PidLidEmail1OriginalEntryId ���K���̃v���p�e�B](pidlidemail1originalentryid-canonical-property.md)
    
- [PidLidEmail2AddressType ���K���̃v���p�e�B](pidlidemail2addresstype-canonical-property.md)
    
- [PidLidEmail2DisplayName ���K���̃v���p�e�B](pidlidemail2displayname-canonical-property.md)
    
- [PidLidEmail2EmailAddress ���K���̃v���p�e�B](pidlidemail2emailaddress-canonical-property.md)
    
- [PidLidEmail2OriginalDisplayName ���K���̃v���p�e�B](pidlidemail2originaldisplayname-canonical-property.md)
    
- [PidLidEmail2OriginalEntryId ���K���̃v���p�e�B](pidlidemail2originalentryid-canonical-property.md)
    
- [PidLidEmail3AddressType ���K���̃v���p�e�B](pidlidemail3addresstype-canonical-property.md)
    
- [PidLidEmail3DisplayName ���K���̃v���p�e�B](pidlidemail3displayname-canonical-property.md)
    
- [PidLidEmail3EmailAddress ���K���̃v���p�e�B](pidlidemail3emailaddress-canonical-property.md)
    
- [PidLidEmail3OriginalDisplayName ���K���̃v���p�e�B](pidlidemail3originaldisplayname-canonical-property.md)
    
- [PidLidEmail3OriginalEntryId ���K���̃v���p�e�B](pidlidemail3originalentryid-canonical-property.md)
    
- [PidLidEmail1DisplayName ���K���̃v���p�e�B](pidlidemail1displayname-canonical-property.md)
    
- [PidLidEmail1OriginalDisplayName ���K���̃v���p�e�B](pidlidemail1originaldisplayname-canonical-property.md)
    
- [PidLidFileUnder ���K���̃v���p�e�B](pidlidfileunder-canonical-property.md)
    
- [PidLidInstantMessagingAddress ���K���̃v���p�e�B](pidlidinstantmessagingaddress-canonical-property.md)
    
- [PidLidWorkAddressCity ���K���̃v���p�e�B](pidlidworkaddresscity-canonical-property.md)
    
- [PidLidWorkAddressCountry ���K���̃v���p�e�B](pidlidworkaddresscountry-canonical-property.md)
    
- [PidLidWorkAddressPostalCode ���K���̃v���p�e�B](pidlidworkaddresspostalcode-canonical-property.md)
    
- [PidLidWorkAddressPostOfficeBox ���K���̃v���p�e�B](pidlidworkaddresspostofficebox-canonical-property.md)
    
- [PidLidWorkAddressState ���K���̃v���p�e�B](pidlidworkaddressstate-canonical-property.md)
    
- [PidLidWorkAddressStreet ���K���̃v���p�e�B](pidlidworkaddressstreet-canonical-property.md)
    
- [PidLidYomiCompanyName ���K���̃v���p�e�B](pidlidyomicompanyname-canonical-property.md)
    
- [PidLidYomiFirstName ���K���̃v���p�e�B](pidlidyomifirstname-canonical-property.md)
    
- [PidLidYomiLastName ���K���̃v���p�e�B](pidlidyomilastname-canonical-property.md)
    
**PSETID_Appointment** ���O��Ԃ̃v���p�e�B�A���̂Ƃ���ł��B 
  
- [PidLidAllAttendeesString ���K���̃v���p�e�B](pidlidallattendeesstring-canonical-property.md)
    
- [PidLidAppointmentCounterProposal ���K���̃v���p�e�B](pidlidappointmentcounterproposal-canonical-property.md)
    
- [PidLidAppointmentDuration ���K���̃v���p�e�B](pidlidappointmentduration-canonical-property.md)
    
- [PidLidAppointmentEndWhole ���K���̃v���p�e�B](pidlidappointmentendwhole-canonical-property.md)
    
- [PidLidAppointmentStartWhole ���K���̃v���p�e�B](pidlidappointmentstartwhole-canonical-property.md)
    
- [PidLidBusyStatus ���K���̃v���p�e�B](pidlidbusystatus-canonical-property.md)
    
- [PidLidCcAttendeesString ���K���̃v���p�e�B](pidlidccattendeesstring-canonical-property.md)
    
- [PidLidLocation ���K���̃v���p�e�B](pidlidlocation-canonical-property.md)
    
- [PidLidRecurring ���K���̃v���p�e�B](pidlidrecurring-canonical-property.md)
    
- [PidLidToAttendeesString ���K���̃v���p�e�B](pidlidtoattendeesstring-canonical-property.md)
    
**PSETID_Common** ���O��Ԃ̃v���p�e�B�A���̂Ƃ���ł��B 
  
- [PidLidCommonEnd ���K���̃v���p�e�B](pidlidcommonend-canonical-property.md)
    
- [PidLidCommonStart ���K���̃v���p�e�B](pidlidcommonstart-canonical-property.md)
    
- [PidLidCompanies ���K���̃v���p�e�B](pidlidcompanies-canonical-property.md)
    
- [PidLidContacts ���K���̃v���p�e�B](pidlidcontacts-canonical-property.md)
    
- [PidLidCustomFlag ���K���̃v���p�e�B](pidlidcustomflag-canonical-property.md)
    
- [PidLidFormPropStream ���K���̃v���p�e�B](pidlidformpropstream-canonical-property.md)
    
- [PidLidFormStorage ���K���̃v���p�e�B](pidlidformstorage-canonical-property.md)
    
- [PidLidHeaderItem ���K���̃v���p�e�B](pidlidheaderitem-canonical-property.md)
    
- [PidLidPageDirStream ���K���̃v���p�e�B](pidlidpagedirstream-canonical-property.md)
    
- [PidLidPropertyDefinitionStream ���K���̃v���p�e�B](pidlidpropertydefinitionstream-canonical-property.md)
    
- [PidLidReminderSet ���K���̃v���p�e�B](pidlidreminderset-canonical-property.md)
    
- [PidLidReminderTime ���K���̃v���p�e�B](pidlidremindertime-canonical-property.md)
    
- [PidLidFlagRequest ���K���̃v���p�e�B](pidlidflagrequest-canonical-property.md)
    
- [PidLidScriptStream ���K���̃v���p�e�B](pidlidscriptstream-canonical-property.md)
    
- [PidLidSmartNoAttach ���K���̃v���p�e�B](pidlidsmartnoattach-canonical-property.md)
    
- [PidLidToDoTitle ���K���̃v���p�e�B](pidlidtodotitle-canonical-property.md)
    
- [PidLidUseTnef ���K���̃v���p�e�B](pidlidusetnef-canonical-property.md)
    
**PSETID_Meeting** ���O��Ԃ̃v���p�e�B�A���̂Ƃ���ł��B 
  
- [PidLidMeetingType ���K���̃v���p�e�B](pidlidmeetingtype-canonical-property.md)
    
**PSETID_Task** ���O��Ԃ̃v���p�e�B�A���̂Ƃ���ł��B 
  
- [PidLidTaskActualEffort ���K���̃v���p�e�B](pidlidtaskactualeffort-canonical-property.md)
    
- [PidLidTaskDueDate ���K���̃v���p�e�B](pidlidtaskduedate-canonical-property.md)
    
- [PidLidTaskEstimatedEffort ���K���̃v���p�e�B](pidlidtaskestimatedeffort-canonical-property.md)
    
- [PidLidTaskFRecurring ���K���̃v���p�e�B](pidlidtaskfrecurring-canonical-property.md)
    
- [PidLidTaskStartDate ���K���̃v���p�e�B](pidlidtaskstartdate-canonical-property.md)
    
- [PidLidTaskStatus ���K���̃v���p�e�B](pidlidtaskstatus-canonical-property.md)
    
**PS_INTERNET_HEADERS** ���O��Ԃ̃v���p�e�B�A���̂Ƃ���ł��B 
  
- [PidTagInternetReturnPath ���K���̃v���p�e�B](pidtaginternetreturnpath-canonical-property.md)
    
**PSETID_Log** ���O��Ԃ̃v���p�e�B�A���̂Ƃ���ł��B 
  
- [PidLidLogDuration ���K���̃v���p�e�B](pidlidlogduration-canonical-property.md)
    
- [PidLidLogEnd ���K���̃v���p�e�B](pidlidlogend-canonical-property.md)
    
- [PidLidLogStart ���K���̃v���p�e�B](pidlidlogstart-canonical-property.md)
    
- [PidLidLogType ���K���̃v���p�e�B](pidlidlogtype-canonical-property.md)
    
**PS_PUBLIC_STRINGS** ���O��Ԃ̃v���p�e�B�A���̂Ƃ���ł��B 
  
- [PidNameKeywords ���K���̃v���p�e�B](pidnamekeywords-canonical-property.md)
    
- [PidNameExchangeJunkEmailMoveStamp 標準プロパティ](pidnameexchangejunkemailmovestamp-canonical-property.md)
    
## <a name="see-also"></a>関連項目



[MAPI 定数](mapi-constants.md)
  
[Outlook がメッセージのヘッダーのみをダウンロードしたかどうかを判別する](how-to-determine-if-outlook-downloaded-only-the-header-of-a-message.md)
  
[連絡先アイテムのメール アドレスを取得する](how-to-get-the-email-address-of-a-contact-item.md)
  
[メッセージと共に保存されているユーザー設定フォーム定義を削除する](how-to-remove-custom-form-definition-saved-with-a-message.md)

