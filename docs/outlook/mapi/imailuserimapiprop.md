---
title: imailuser imapiprop
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMailUser
api_type:
- COM
ms.assetid: 74c25870-62d9-484a-9a99-4dc35c52479e
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a0e109fe95120483e700bab5b82f6d7cb75e2e28
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351401"
---
# <a name="imailuser--imapiprop"></a>IMailUser : IMAPIProp

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージングユーザーに関連付けられている多くのプロパティへのアクセスを提供します。 **imailuser**インターフェイスは、メッセージングユーザーオブジェクトによって実装されます。 **imailuser**は、 [imapiprop: IUnknown](imapipropiunknown.md)インターフェイスから継承し、独自の独自のメソッドはありません。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|公開者:  <br/> |メッセージングユーザーオブジェクト  <br/> |
|実装元:  <br/> |アドレス帳プロバイダー  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーション  <br/> |
|インターフェイス識別子:  <br/> |IID_IMailUser  <br/> |
|ポインターの種類:  <br/> |lpmailuser  <br/> |
|トランザクションモデル:  <br/> |一括  <br/> |
   
## <a name="vtable-order"></a>v の順序

このインターフェイスには一意のメソッドはありません。
  
|**必須のプロパティ**|**Access**|
|:-----|:-----|
|**PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |読み取り/書き込み  <br/> |
|**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |読み取り/書き込み  <br/> |
|**PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_EMAIL_ADDRESS**([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |読み取り/書き込み  <br/> |
|**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_RECORD_KEY**([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_SEARCH_KEY**([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |読み取り専用  <br/> |
   
## <a name="remarks"></a>解説

必要なプロパティの5つは、受信者のベースアドレスプロパティと呼ばれます。
  
- **PR_ADDRTYPE**
    
- **PR_DISPLAY_NAME**
    
- **PR_EMAIL_ADDRESS**
    
- **PR_ENTRYID**
    
- **PR_SEARCH_KEY**
    
これらのプロパティは、類似したプロパティの他の多くのグループがこの基本グループに基づいて構築されるため、特別なものと見なされます。 他のグループは、メッセージの元の送信者や代理人の送信者など、さまざまな役割で受信者を表すために使用されます。 これらのプロパティの詳細と使用方法については、「 [MAPI アドレスの種類](mapi-address-types.md)」を参照してください。
  
メッセージングユーザーは、 **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) プロパティをサポートすることによって、それらのプロパティのコレクションを表示できます。 **PR_DETAILS_TABLE**は、[詳細] ダイアログボックスのレイアウト、または受信者プロパティ情報を表示するタブ付きプロパティページを説明する表示テーブルです。 MAPI は、クライアントが[IAddrBook::D etails](iaddrbook-details.md)メソッドを呼び出すときに、詳細ダイアログボックスを作成します。 
  
メッセージングユーザーオブジェクトには、その他のオプションプロパティを関連付けることができます。 MAPI は、メッセージングユーザーに関する追加のアドレス指定情報を提供する多くのプロパティを定義します。 これらのプロパティはすべて文字列です。 次のリストは、よく使用されるプロパティを示しています。
  
- **PR_ACCOUNT**([PidTagAccount](pidtagaccount-canonical-property.md)) 
    
- **PR_ASSISTANT**([PidTagAssistant](pidtagassistant-canonical-property.md)) 
    
- **PR_BUSINESS_TELEPHONE_NUMBER**([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md)) 
    
- **PR_GIVEN_NAME**([PidTagGivenName](pidtaggivenname-canonical-property.md)) 
    
- **PR_GOVERNMENT_ID_NUMBER**([PidTagGovernmentIdNumber](pidtaggovernmentidnumber-canonical-property.md)) 
    
- **PR_LOCALITY**([PidTagLocality](pidtaglocality-canonical-property.md)) 
    
- **PR_POSTAL_ADDRESS**([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md)) 
    
プロパティの完全な一覧については、「[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

