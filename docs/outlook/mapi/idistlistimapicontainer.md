---
title: idistlist IMAPIContainer
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
  
変更可能なアドレス帳コンテナー内の配布リストへのアクセスを提供します。 **idistlist**では、名前解決を実行するだけでなく、配布リストの作成、コピー、および削除を行うことができます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|公開者:  <br/> |配布リストオブジェクト  <br/> |
|実装元:  <br/> |アドレス帳プロバイダー  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーション  <br/> |
|インターフェイス識別子:  <br/> |IID_IDistList  <br/> |
|ポインターの種類:  <br/> |lpdistlist  <br/> |
|トランザクションモデル:  <br/> |一括  <br/> |
   
## <a name="vtable-order"></a>v の順序

このインターフェイスには一意のメソッドはありません。
  
|**必須のプロパティ**|**Access**|
|:-----|:-----|
|**PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |読み取り/書き込み  <br/> |
|**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |読み取り/書き込み  <br/> |
|**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_RECORD_KEY**([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |読み取り専用  <br/> |
   
## <a name="remarks"></a>注釈

**idistlist**インターフェイスは[IMAPIContainer](imapicontainerimapiprop.md)から継承され、アドレス帳コンテナーと同じメソッドを含みます。 そのため、 **idistlist**インターフェイスのメソッドは[IABContainer](iabcontainerimapicontainer.md)インターフェイスのメソッドと同じなので、ここでは複製されません。 
  
**idistlist**を実装する配布リストまたはオブジェクトは、メッセージングユーザーオブジェクトまたは個々の受信者のコレクションです。 配布リストは、すべてのメッセージングユーザーオブジェクト、または一部のメッセージングユーザーと一部の配布リストで構成できます。 
  
通常、配布リストには次の2つの種類があります。
  
- 基礎となるメッセージングシステムによって展開された配布リスト。 この種類のリストには、 **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) という住所があり、個別の受信者と同じように処理されます。 
    
- ローカルコンテナーに存在し、クライアントアプリケーションによって拡張された配布リスト。
    
オプションの配布リストのプロパティは次のとおりです。
  
- **PR_LAST_MODIFICATION_TIME**([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))
    
- **PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) 
    
- **PR_DETAILS_TABLE**([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) 
    
**PR_ADDRTYPE**は必須ですが、 **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) は必須ではないことに注意してください。 これは、電子メールアドレスのない配布リストでもメッセージを受信できるが、そのメンバーリストを展開する必要があるためです。 **PR_ADDRTYPE**プロパティが mapipdl に設定されている場合、MAPI は拡張を実行します。 **PR_ADDRTYPE**が mapipdl 以外の値の場合は、トランスポートプロバイダーが拡張を実行します。 
  
**idistlist**メソッドの使用方法の詳細については、 **IABContainer**の parallel メソッドの参照エントリを参照してください。
  
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

