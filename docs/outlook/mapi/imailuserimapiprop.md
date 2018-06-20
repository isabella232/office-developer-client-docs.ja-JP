---
title: IMailUser IMAPIProp
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 0c70d16d294426d30f3ac5f00b6bc46992386a86
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800447"
---
# <a name="imailuser--imapiprop"></a>IMailUser: IMAPIProp

  
  
**適用されます**: Outlook 
  
メッセージング ユーザーに関連付けられている多くのプロパティへのアクセスを提供します。 **IMailUser**インターフェイスは、メッセージング ユーザーのオブジェクトによって実装されます。 **IMailUser**を継承、 [IMAPIProp: IUnknown](imapipropiunknown.md)インタ フェースし、独自の一意のメソッドがありません。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|によって公開されます。  <br/> |メッセージングのユーザー オブジェクト  <br/> |
|によって実装されます。  <br/> |アドレス帳プロバイダー  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーション  <br/> |
|インターフェイスの識別子。  <br/> |IID_IMailUser  <br/> |
|ポインターの型。  <br/> |LPMAILUSER  <br/> |
|トランザクション モデル:  <br/> |トランザクション処理  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

このインターフェイスには、固有のメソッドがありません。
  
|**必要なプロパティ**|**Access**|
|:-----|:-----|
|**PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |値の取得および設定が可能です。  <br/> |
|**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |値の取得および設定が可能です。  <br/> |
|**PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |値の取得のみ可能です。  <br/> |
|**PR_EMAIL_ADDRESS**([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |値の取得および設定が可能です。  <br/> |
|**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |値の取得のみ可能です。  <br/> |
|**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |値の取得のみ可能です。  <br/> |
|**PR_RECORD_KEY**([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |値の取得のみ可能です。  <br/> |
|**PR_SEARCH_KEY**([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |値の取得のみ可能です。  <br/> |
   
## <a name="remarks"></a>備考

受信者のベース アドレス プロパティとして 5 つの必須プロパティの確認されています。
  
- **PR_ADDRTYPE**
    
- **PR_DISPLAY_NAME**
    
- **PR_EMAIL_ADDRESS**
    
- **PR_ENTRYID**
    
- **PR_SEARCH_KEY**
    
これらのプロパティは他の多くのようなプロパティのグループは、この基本のグループに基づいて構築するため、特別なと見なされます。 他のグループのさまざまな役割は、受信者を記述するなど、メッセージの元または送信者に委任されます。 これらのプロパティとその使用方法に関する詳細については、 [MAPI のアドレスの種類](mapi-address-types.md)を参照してください。
  
メッセージング ユーザーは**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) のプロパティをサポートすることにより、それらのプロパティのコレクションを表示できます。 **PR_DETAILS_TABLE**は、[詳細] ダイアログ ボックスまたは受信者のプロパティ情報を表示するタブ付きプロパティ ページのレイアウトを記述するディスプレイ テーブルです。 MAPI では、クライアントは、 [IAddrBook::Details](iaddrbook-details.md)メソッドを呼び出すと、詳細情報がダイアログ ボックスに作成されます。 
  
ユーザー オブジェクトをメッセージに関連するその他のオプションのプロパティを設定できます。 MAPI は、メッセージングのユーザーに関するその他のアドレス情報を提供する多くのプロパティを定義します。 すべてのこれらのプロパティは、文字の文字列です。 一般的に使用されるプロパティを次に示します。
  
- **PR_ACCOUNT**([PidTagAccount](pidtagaccount-canonical-property.md)) 
    
- **PR_ASSISTANT**([PidTagAssistant](pidtagassistant-canonical-property.md)) 
    
- **PR_BUSINESS_TELEPHONE_NUMBER**([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md)) 
    
- **PR_GIVEN_NAME**([PidTagGivenName](pidtaggivenname-canonical-property.md)) 
    
- **PR_GOVERNMENT_ID_NUMBER**([PidTagGovernmentIdNumber](pidtaggovernmentidnumber-canonical-property.md)) 
    
- **PR_LOCALITY**([PidTagLocality](pidtaglocality-canonical-property.md)) 
    
- **PR_POSTAL_ADDRESS**([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md)) 
    
プロパティの一覧については、 [MAPI の名前を標準のプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[MAPI インターフェイス](mapi-interfaces.md)

