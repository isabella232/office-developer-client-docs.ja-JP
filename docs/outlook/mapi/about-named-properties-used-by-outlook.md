---
title: "Outlook �Ŏg�p���閼�O�t���̃v���p�e�B�ɂ\x82���"
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8c245ec2-bb18-ecf0-b4ad-8c164c5924cf
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: aa4d52d25f120e8b3e2a4c0dcaa4845ad576127a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566230"
---
# <a name="about-named-properties-used-by-outlook"></a>Outlook �Ŏg�p���閼�O�t���̃v���p�e�B�ɂ���

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
MAPI �ł́A����̃v���p�e�B�ɖ��O����蓖�Ă�A�ŗL�̎��ʎq����̖��O��}�b�s���O���邽�߁A�Z�b�V�����̊Ԃŉi���I�Ȃ��̖��O�̎��ʎq�̃}�b�s���O��쐬���邽�߂̋@�\��񋟂��܂��B���O�t���v���p�e�B�́A���O�ƃv���p�e�B�̐ݒ�̃O���[�o���Ɉ�ӂ̎��ʎq (GUID) �ɂ���Ď��ʂ��܂��B���O�ɂ́A���l�܂��͕����񂪂ł��܂��BMicrosoft Outlook 2013�܂���Microsoft Outlook 2010�v���p�e�B�̐ݒ��Outlook 2013�܂���Outlook 2010�A **PSETID_Appointment** �Ȃǂɂ���Ē�`���ꂽ���O��Ԃł͑����̏ꍇ�B 
  
���O�t���̃v���p�e�B�𑀍삷��ɂ́A [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)�֐���[IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)�֐���g�p���܂��B���O�� GUID �v���p�e�B�̐ݒ�́A���݂� MAPI �Z�b�V�����͗L���ȃv���p�e�B���ʎq��擾����[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)�֐��ɓn����܂��B���̃v���p�e�B�̎��ʎq���R���s���[�^�[����ʂ̃R���s���[�^�[�ɈقȂ邱�Ƃ��ł��܂��݈̂�ѐ��̂��閼�O�t���̃v���p�e�B�ɃA�N�Z�X������@�ł́A���̖��O�� GUID �v���p�e�B���킩���Ă��܂��B ���ʎq�͈̔͂́A��� 0x8000 �� 0 xfffe �͈́B 
  
[IMAPIProp: IUnknown](imapipropiunknown.md)�C���^�[�t�F�C�X���������C�ӂ̃I�u�W�F�N�g�́A���O�t���̃v���p�e�B��T�|�[�g�ł��܂��B��̓I�ɂ́AMAPI �T�[�r�X �v���o�C�[�[�܂��� mapi �́A���O�t���̃v���p�e�B�̒l��擾����[IMAPIProp::GetProps](imapiprop-getprops.md)���������K�v������܂��B���� MAPI �v���o�C�](imapiprop-getprops.md)�[��ڋq�Ƌ��L����Ă���f�[�^��j���̃��X�N�̗��R�ɂ��A���O�t��Outlook 2013�܂���Outlook 2010�ɂ���Ďg�p�����v���p�e�B�̐ݒ�̓T�|�[�g����Ă��܂���B 
  
Outlook 2013 および Outlook 2010 は、MAPI 名前付きプロパティなど、その機能の多くを実装するために、添付ファイルのセキュリティおよび会議の代替日時を使用します。 この基になるデータでは、上記 2013 の Outlook と Outlook 2010 これらのプロパティの一部として公開、Outlook 2013 と Outlook 2010 のオブジェクト モデル内のアイテムのプロパティです。 たとえば、オブジェクト モデルでは、 **ContactItem**オブジェクトの**Email1Address**プロパティは、 **PSETID_Address**名前空間の名前付きの[PidLidEmail1EmailAddress の標準的なプロパティ](pidlidemail1emailaddress-canonical-property.md)に対応します。 ですが、一般的に、互換性とデータの整合性の問題が発生したため Outlook 2013 および Outlook 2010 で使用される MAPI プロパティの多くに公開されていないオブジェクト モデルです。 
  
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
    
- [PidNameExchangeJunkEmailMoveStamp ���K���̃v���p�e�B](pidnameexchangejunkemailmovestamp-canonical-property.md)
    
## <a name="see-also"></a>�֘A����



[MAPI �萔](mapi-constants.md)
  
[Outlook がメッセージのヘッダーのみをダウンロードしたかどうかを判別する](how-to-determine-if-outlook-downloaded-only-the-header-of-a-message.md)
  
[連絡先アイテムのメール アドレスを取得する](how-to-get-the-email-address-of-a-contact-item.md)
  
[メッセージと共に保存されているユーザー設定フォーム定義を削除する](how-to-remove-custom-form-definition-saved-with-a-message.md)

