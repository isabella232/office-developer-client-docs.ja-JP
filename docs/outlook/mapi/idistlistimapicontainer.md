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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 463d81a6692b6071cada0ad22e7343020563e41c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431548"
---
# <a name="idistlist--imapicontainer"></a>IDistList : IMAPIContainer

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
変更可能なアドレス帳コンテナー内の配布リストへのアクセスを提供します。 **IDistList は** 、名前解決の実行に加えて、配布リストを作成、コピー、および削除できます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|次のユーザーによって公開されます。  <br/> |配布リスト オブジェクト  <br/> |
|実装元:  <br/> |アドレス帳プロバイダー  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーション  <br/> |
|インターフェイス識別子:  <br/> |IID_IDistList  <br/> |
|ポインターの種類:  <br/> |LPDISTLIST  <br/> |
|トランザクション モデル:  <br/> |Transacted  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

このインターフェイスには、一意のメソッドが含まれる必要があります。
  
|**必須のプロパティ**|**Access**|
|:-----|:-----|
|**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |読み取り/書き込み  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |読み取り/書き込み  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |読み取り専用  <br/> |
   
## <a name="remarks"></a>注釈

**IDistList インターフェイスは** [IMAPIContainer](imapicontainerimapiprop.md)から継承され、アドレス帳コンテナーと同じメソッドが含まれています。 したがって **、IDistList** インターフェイスのメソッドは [IABContainer](iabcontainerimapicontainer.md) インターフェイスのメソッドと同じであるため、ここでは重複されません。 
  
**IDistList** を実装する配布リストまたはオブジェクトは、メッセージング ユーザー オブジェクトまたは個々の受信者のコレクションです。 配布リストは、すべてのメッセージング ユーザー オブジェクト、または一部のメッセージング ユーザーと一部の配布リストで構成できます。 
  
通常、配布リストには次の 2 種類があります。
  
- 基になるメッセージング システムによって展開される配布リスト。 この種類のリストには、アドレス PR_EMAIL_ADDRESS **(** [PidTagEmailAddress)](pidtagemailaddress-canonical-property.md)が含まれるので、個々の受信者と同じように扱います。 
    
- ローカル コンテナー内に存在し、クライアント アプリケーションによって展開される配布リスト。
    
オプションの配布リスト プロパティには、次のものが含まれます。
  
- **PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) 
    
- **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) 
    
この設定 **PR_ADDRTYPE** 必須ですが、PR_EMAIL_ADDRESS **(** [PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) は必須ではありません。 これは、電子メール アドレスのない配布リストはメッセージを受信できますが、そのメンバー リストを展開する必要があるためです。 このプロパティ **PR_ADDRTYPE** MAPIPDL に設定されている場合、MAPI は展開を実行します。 この **PR_ADDRTYPE** MAPIPDL 以外の値である場合、トランスポート プロバイダーは拡張を実行します。 
  
**IDistList** メソッドを使用する方法の詳細については **、IABContainer** の並列メソッドのリファレンス エントリを参照してください。
  
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

