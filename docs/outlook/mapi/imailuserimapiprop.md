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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a0e109fe95120483e700bab5b82f6d7cb75e2e28
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436595"
---
# <a name="imailuser--imapiprop"></a>IMailUser : IMAPIProp

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージング ユーザーに関連付けられている多くのプロパティへのアクセスを提供します。 **IMailUser インターフェイスは**、メッセージング ユーザー オブジェクトによって実装されます。 **IMailUser は** [IMAPIProp : IUnknown](imapipropiunknown.md) インターフェイスから継承され、独自の固有のメソッドはありません。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|次のユーザーによって公開されます。  <br/> |メッセージング ユーザー オブジェクト  <br/> |
|実装元:  <br/> |アドレス帳プロバイダー  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーション  <br/> |
|インターフェイス識別子:  <br/> |IID_IMailUser  <br/> |
|ポインターの種類:  <br/> |LPMAILUSER  <br/> |
|トランザクション モデル:  <br/> |Transacted  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

このインターフェイスには、一意のメソッドが含まれる必要があります。
  
|**必須のプロパティ**|**Access**|
|:-----|:-----|
|**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |読み取り/書き込み  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |読み取り/書き込み  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |読み取り/書き込み  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |読み取り専用  <br/> |
   
## <a name="remarks"></a>注釈

必要なプロパティの 5 つを、受信者の基本アドレス プロパティと呼ばれる。
  
- **PR_ADDRTYPE**
    
- **PR_DISPLAY_NAME**
    
- **PR_EMAIL_ADDRESS**
    
- **PR_ENTRYID**
    
- **PR_SEARCH_KEY**
    
これらのプロパティは、この基本グループの上に類似するプロパティの他の多くのグループが構築されているので、特別と見なされます。 他のグループは、メッセージの元の送信者や代理人の送信者など、さまざまな役割の受信者を記述するために使用されます。 これらのプロパティとそれらを使用する方法の詳細については、「MAPI アドレスの種類 [」を参照してください](mapi-address-types.md)。
  
メッセージング ユーザーは、プロパティ ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md) **)** プロパティをサポートPR_DETAILS_TABLEプロパティのコレクションを表示できます。 **PR_DETAILS_TABLE** は、詳細ダイアログ ボックスのレイアウト、または受信者のプロパティ情報を表示するタブ付きプロパティ ページを示す表示テーブルです。 MAPI は、クライアントが [IAddrBook::Dメソッドを呼び出:Dダイアログ ボックスを作成](iaddrbook-details.md) します。 
  
メッセージング ユーザー オブジェクトには、他の省略可能なプロパティを関連付けできます。 MAPI は、メッセージング ユーザーに関する追加のアドレス情報を提供する多くのプロパティを定義します。 これらのプロパティはすべて文字列です。 次の一覧は、より一般的に使用されるプロパティを示しています。
  
- **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) 
    
- **PR_ASSISTANT** ([PidTagAssistant](pidtagassistant-canonical-property.md)) 
    
- **PR_BUSINESS_TELEPHONE_NUMBER** ([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md)) 
    
- **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) 
    
- **PR_GOVERNMENT_ID_NUMBER** ([PidTagGovernmentIdNumber](pidtaggovernmentidnumber-canonical-property.md)) 
    
- **PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md)) 
    
- **PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md)) 
    
プロパティの完全な一覧については [、「Mapping Canonical Property Names to MAPI Names」を参照してください](mapping-canonical-property-names-to-mapi-names.md)。
  
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

