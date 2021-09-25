---
title: IAttach IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAttach
api_type:
- COM
ms.assetid: f47e20e1-2a30-4c9e-8ca6-e8c5e72f44a1
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c67ce8be8cd1389a985f8762759a0136c5f81c1b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580042"
---
# <a name="iattach--imapiprop"></a>IAttach : IMAPIProp

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ内の添付ファイルのプロパティへのアクセスを維持し、提供します。 **IAttach インターフェイス** には独自のメソッドはありません。 添付ファイルの使用方法の詳細については、「MAPI 添付ファイルと[添付ファイルテーブル」](mapi-attachments.md)[を参照してください](attachment-tables.md)。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|次のユーザーによって公開されます。  <br/> |添付ファイル オブジェクト  <br/> |
|実装元:  <br/> |メッセージ ストア プロバイダー  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーション  <br/> |
|インターフェイス識別子:  <br/> |IID_IAttachment  <br/> |
|ポインターの種類:  <br/> |LPATTACH  <br/> |
|トランザクション モデル:  <br/> |Transacted  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

このインターフェイスには、一意のメソッドが含まれる必要があります。
  
|**必須のプロパティ**|**Access**|
|:-----|:-----|
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))  <br/> |読み取り/書き込み  <br/> |
|**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))  <br/> |読み取り/書き込み  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

