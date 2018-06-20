---
title: IDistList IMAPIContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IDistList
api_type:
- COM
ms.assetid: bd8e1ddb-3027-428b-8964-81614f80282d
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 7fee3c84d6a4d4a94397f5197f45637b0c7dd2be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800433"
---
# <a name="idistlist--imapicontainer"></a>IDistList: IMAPIContainer

  
  
**適用されます**: Outlook 
  
本コンテナーの変更可能なアドレスでの配布リストへのアクセスを提供します。 **IDistList**は、作成、コピー、および名前解決を実行するだけでなく、配布リストを削除できます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|によって公開されます。  <br/> |配布リスト オブジェクト  <br/> |
|によって実装されます。  <br/> |アドレス帳プロバイダー  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーション  <br/> |
|インターフェイスの識別子。  <br/> |IID_IDistList  <br/> |
|ポインターの型。  <br/> |LPDISTLIST  <br/> |
|トランザクション モデル:  <br/> |トランザクション処理  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

このインターフェイスには、固有のメソッドがありません。
  
|**必要なプロパティ**|**Access**|
|:-----|:-----|
|**PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |値の取得および設定が可能です。  <br/> |
|**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |値の取得および設定が可能です。  <br/> |
|**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |値の取得のみ可能です。  <br/> |
|**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |値の取得のみ可能です。  <br/> |
|**PR_RECORD_KEY**([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |値の取得のみ可能です。  <br/> |
   
## <a name="remarks"></a>備考

**IDistList**インターフェイスは、 [IMAPIContainer](imapicontainerimapiprop.md)を継承し、アドレス帳コンテナーと同じメソッドが含まれています。 したがって、 **IDistList**インターフェイスのメソッドは、[これにより](iabcontainerimapicontainer.md)インタ フェースのものと同一であるため、これらが重複していないここでは。 
  
配布リストまたは**IDistList**を実装するオブジェクトは、メッセージングのユーザー オブジェクトまたは個々 の受信者のコレクションです。 配布リストは、メッセージのすべてのユーザー オブジェクトまたはいくつかのメッセージングのユーザーといくつかの配布リストで構成されます。 
  
通常は、配布リストの 2 つの種類があります。
  
- 基になるメッセージング システムによって展開される配布リストです。 この種類の一覧のアドレス、 **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) には、個々 の受信者の場合と同じに扱われます。 
    
- ローカル コンテナー内に存在し、クライアント アプリケーションが展開されている配布リストです。
    
省略可能な配布リストのプロパティを以下に示します。
  
- **PR_LAST_MODIFICATION_TIME**([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))
    
- **PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) 
    
- **PR_DETAILS_TABLE**([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) 
    
**PR_ADDRTYPE**が必要ですが、 **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) ではないことを確認します。 電子メール アドレス、配布リストは、メッセージを受信もできますが、[メンバー] ボックスの一覧を展開する必要があるためにです。 **PR_ADDRTYPE**プロパティは、MAPIPDL に設定されている場合、MAPI は、拡張を実行します。 **PR_ADDRTYPE**が MAPIPDL 以外の値の場合は、トランスポート プロバイダーは、拡張を実行します。 
  
**IDistList**メソッドを使用する方法の詳細については、**これにより**の並列メソッドの参照のエントリを参照してください。
  
## <a name="see-also"></a>関連項目



[MAPI インターフェイス](mapi-interfaces.md)

