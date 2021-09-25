---
title: MAPI の追加について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 78e2806d-bb6f-cd96-21f1-b7c667c73c33
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 033053c41988ad9b63f88def7652d1a37dae5f1e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588309"
---
# <a name="about-mapi-additions"></a>MAPI の追加について

**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI の追加は、以前は MAPI プログラマリファレンスの一部として公開および文書化されていないデータ型、関数、プロパティなど、メッセージング アプリケーション プログラミング インターフェイス (MAPI) に属する API です。 これらの定義には、次の定義とプロパティが含まれます。
  
## <a name="constant-definitions"></a>定数の定義

- **[その他の MAPI 定数](mapi-constants.md)**
  
## <a name="data-types"></a>データ型

- **[EXCHANGE_STORE_VERSION_NUM](exchange_store_version_num.md)**
    
- **[FollowUpStatus](followupstatus.md)**
    
- **[性別](gender.md)**
    
- **[OlFlagIcon](olflagicon.md)**
    
## <a name="functions"></a>関数

- **[FixMAPI](fixmapi.md)**
    
## <a name="properties"></a>プロパティ

通常、次のプロパティはメッセージ オブジェクトによって公開されます。
  
- **[PR_BODY_W](pidtagbody-canonical-property.md)**
    
- **[PR_CONFLICT_ITEMS](pidtagconflictitems-canonical-property.md)**
    
- **[PR_DISPLAY_BCC_W](pidtagdisplaybcc-canonical-property.md)**
    
- **[PR_DISPLAY_CC_W](pidtagdisplaycc-canonical-property.md)**
    
- **[PR_DISPLAY_TO_W](pidtagdisplayto-canonical-property.md)**
    
- **[PR_FLAG_STATUS](pidtagflagstatus-canonical-property.md)**
    
- **[PR_FOLLOWUP_ICON](pidtagfollowupicon-canonical-property.md)**
    
- **[PR_INETMAIL_OVERRIDE_FORMAT](pidtaginternetmailoverrideformat-canonical-property.md)**
    
- **[PR_MESSAGE_CLASS_W](pidtagmessageclass-canonical-property.md)**
    
- **[PR_MSG_EDITOR_FORMAT](pidtagmessageeditorformat-canonical-property.md)**
    
- **[PR_NORMALIZED_SUBJECT_W](pidtagnormalizedsubject-canonical-property.md)**
    
- **[PR_SENDER_ADDRTYPE_W](pidtagsenderaddresstype-canonical-property.md)**
    
- **[PR_SENDER_EMAIL_ADDRESS_W](pidtagsenderemailaddress-canonical-property.md)**
    
- **[PR_SENDER_NAME_W](pidtagsendername-canonical-property.md)**
    
- **[PR_SENT_REPRESENTING_ADDRTYPE_W](pidtagsentrepresentingaddresstype-canonical-property.md)**
    
- **[PR_SENT_REPRESENTING_EMAIL_ADDRESS_W](pidtagsentrepresentingemailaddress-canonical-property.md)**
    
- **[PR_SENT_REPRESENTING_NAME_W](pidtagsentrepresentingname-canonical-property.md)**
    
- **[PR_SUBJECT_PREFIX_W](pidtagsubjectprefix-canonical-property.md)**
    
- **[PR_SUBJECT_W](pidtagsubject-canonical-property.md)**
    
次のプロパティは、アドレス帳のコンテンツ テーブル オブジェクトによって公開されます。
  
- **[PR_DISPLAY_TYPE_EX](pidtagdisplaytypeex-canonical-property.md)**
    
次のプロパティは、アドレス帳コンテナー オブジェクトによって公開されます。
  
- **[PR_EMS_AB_SERVER](pidtagemsabserver-canonical-property.md)**
    
- **[PR_EMS_AB_SERVER_A](pidtagemsabserver-canonical-property.md)**
    
- **[PR_EMS_AB_SERVER_W](pidtagemsabserver-canonical-property.md)**
    
次のプロパティは、フォルダー オブジェクトによって公開されます。
  
- **[PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)**
    
- **[PR_AGING_PERIOD](pidtagagingperiod-canonical-property.md)**
    
次のプロパティは、メッセージング ユーザー オブジェクトによって公開されます。
  
- **[PR_ASSISTANT_TELEPHONE_NUMBER_W](pidtagassistanttelephonenumber-canonical-property.md)**
    
- **[PR_ASSISTANT_W](pidtagassistant-canonical-property.md)**
    
- **[PR_ATTACHMENT_CONTACTPHOTO](pidtagattachmentcontactphoto-canonical-property.md)**
    
- **[PR_BIRTHDAY](pidtagbirthday-canonical-property.md)**
    
- **[PR_BUSINESS_FAX_NUMBER_W](pidtagbusinessfaxnumber-canonical-property.md)**
    
- **[PR_BUSINESS_HOME_PAGE_W](pidtagbusinesshomepage-canonical-property.md)**
    
- **[PR_CALLBACK_TELEPHONE_NUMBER_W](pidtagcallbacktelephonenumber-canonical-property.md)**
    
- **[PR_CAR_TELEPHONE_NUMBER_W](pidtagcartelephonenumber-canonical-property.md)**
    
- **[PR_CELLULAR_TELEPHONE_NUMBER_W](pidtagmobiletelephonenumber-canonical-property.md)**
    
- **[PR_CHILDRENS_NAMES_W](pidtagchildrensnames-canonical-property.md)**
    
- **[PR_DEPARTMENT_NAME_W](pidtagdepartmentname-canonical-property.md)**
    
- **[PR_DISPLAY_NAME_PREFIX_W](pidtagdisplaynameprefix-canonical-property.md)**
    
- **[PR_GENDER](pidtaggender-canonical-property.md)**
    
- **[PR_GENERATION_W](pidtaggeneration-canonical-property.md)**
    
- **[PR_GIVEN_NAME_W](pidtaggivenname-canonical-property.md)**
    
- **[PR_HOBBIES_W](pidtaghobbies-canonical-property.md)**
    
- **[PR_HOME_ADDRESS_CITY_W](pidtaghomeaddresscity-canonical-property.md)**
    
- **[PR_HOME_ADDRESS_COUNTRY_W](pidtaghomeaddresscountry-canonical-property.md)**
    
- **[PR_HOME_ADDRESS_POST_OFFICE_BOX_W](pidtaghomeaddresspostofficebox-canonical-property.md)**
    
- **[PR_HOME_ADDRESS_POSTAL_CODE_W](pidtaghomeaddresspostalcode-canonical-property.md)**
    
- **[PR_HOME_ADDRESS_STATE_OR_PROVINCE_W](pidtaghomeaddressstateorprovince-canonical-property.md)**
    
- **[PR_HOME_ADDRESS_STREET_W](pidtaghomeaddressstreet-canonical-property.md)**
    
- **[PR_HOME_FAX_NUMBER_W](pidtaghomefaxnumber-canonical-property.md)**
    
- **[PR_HOME_TELEPHONE_NUMBER_W](pidtaghometelephonenumber-canonical-property.md)**
    
- **[PR_KEYWORD_W](pidtagkeyword-canonical-property.md)**
    
- **[PR_MANAGER_NAME_W](pidtagmanagername-canonical-property.md)**
    
- **[PR_MIDDLE_NAME_W](pidtagmiddlename-canonical-property.md)**
    
- **[PR_NICKNAME_W](pidtagnickname-canonical-property.md)**
    
- **[PR_OFFICE_LOCATION_W](pidtagofficelocation-canonical-property.md)**
    
- **[PR_OFFICE_TELEPHONE_NUMBER_W](pidtagbusinesstelephonenumber-canonical-property.md)**
    
- **[PR_OTHER_ADDRESS_CITY_W](pidtagotheraddresscity-canonical-property.md)**
    
- **[PR_OTHER_ADDRESS_COUNTRY_W](pidtagotheraddresscountry-canonical-property.md)**
    
- **[PR_OTHER_ADDRESS_POST_OFFICE_BOX_W](pidtagotheraddresspostofficebox-canonical-property.md)**
    
- **[PR_OTHER_ADDRESS_POSTAL_CODE_W](pidtagotheraddresspostalcode-canonical-property.md)**
    
- **[PR_OTHER_ADDRESS_STATE_OR_PROVINCE_W](pidtagotheraddressstateorprovince-canonical-property.md)**
    
- **[PR_OTHER_ADDRESS_STREET_W](pidtagotheraddressstreet-canonical-property.md)**
    
- **[PR_PAGER_TELEPHONE_NUMBER_W](pidtagpagertelephonenumber-canonical-property.md)**
    
- **[PR_PERSONAL_HOME_PAGE_W](pidtagpersonalhomepage-canonical-property.md)**
    
- **[PR_PRIMARY_TELEPHONE_NUMBER_W](pidtagprimarytelephonenumber-canonical-property.md)**
    
- **[PR_PROFESSION_W](pidtagprofession-canonical-property.md)**
    
- **[PR_SPOUSE_NAME_W](pidtagspousename-canonical-property.md)**
    
- **[PR_SURNAME_W](pidtagsurname-canonical-property.md)**
    
- **[PR_TITLE_W](pidtagtitle-canonical-property.md)**
    
- **[PR_TTYTDD_PHONE_NUMBER_W](pidtagttytddphonenumber-canonical-property.md)**
    
- **[PR_WEDDING_ANNIVERSARY](pidtagweddinganniversary-canonical-property.md)**
    
次のプロパティは、プロファイル セクション オブジェクトによって公開されます。
  
- **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)**
    
- **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)**
    
- **[PR_PROVIDER_DISPLAY_NAME_W](pidtagproviderdisplayname-canonical-property.md)**
    
- **[PR_PROVIDER_ICON_W](pidtagprovidericon-canonical-property.md)**
    
- **[PR_ROH_FLAGS](pidtagrpcoverhttpflags-canonical-property.md)**
    
- **[PR_ROH_PROXY_AUTH_SCHEME](pidtagrpcoverhttpproxyauthscheme-canonical-property.md)**
    
- **[PR_ROH_PROXY_PRINCIPAL_NAME](pidtagrpcoverhttpproxyprincipalname-canonical-property.md)**
    
- **[PR_ROH_PROXY_SERVER](pidtagrpcoverhttpproxyserver-canonical-property.md)**
    
次のプロパティは、ストア オブジェクトによって公開されます。
  
- **[PR_IPM_APPOINTMENT_ENTRYID](pidtagipmappointmententryid-canonical-property.md)**
    
- **[PR_IPM_CONTACT_ENTRYID](pidtagipmcontactentryid-canonical-property.md)**
    
- **[PR_IPM_DRAFTS_ENTRYID](pidtagipmdraftsentryid-canonical-property.md)**
    
- **[PR_IPM_JOURNAL_ENTRYID](pidtagipmjournalentryid-canonical-property.md)**
    
- **[PR_IPM_NOTE_ENTRYID](pidtagipmnoteentryid-canonical-property.md)**
    
- **[PR_IPM_TASK_ENTRYID](pidtagipmtaskentryid-canonical-property.md)**
    
次のプロパティは、ストア オブジェクトによって公開され、ストア上の電子メールの特定の要素を検索する場合に使用されます。
  
- **[PR_SEARCH_ATTACHMENTS_W](pidtagsearchattachments-canonical-property.md)**
    
- **[PR_SEARCH_RECIP_EMAIL_BCC_W](pidtagsearchrecipientemailbcc-canonical-property.md)**
    
- **[PR_SEARCH_RECIP_EMAIL_CC_W](pidtagsearchrecipientemailcc-canonical-property.md)**
    
- **[PR_SEARCH_RECIP_EMAIL_TO_W](pidtagsearchrecipientemailto-canonical-property.md)**
    
## <a name="see-also"></a>関連項目

- [Outlook が Exchange キャッシュ モードの場合にリモート サーバーでストアにアクセスする](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)  
- [プロファイル内のバージョンExchange Server検出Outlookする](how-to-detect-the-version-of-exchange-server-in-an-outlook-profile.md)
- [Outlook が Exchange キャッシュ モードの場合にリモート サーバーでストアを開く](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [Exchange キャッシュ モードで同期を呼び出すことなく OST でメッセージを管理する](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

