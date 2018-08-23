---
title: IAttach IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAttach
api_type:
- COM
ms.assetid: f47e20e1-2a30-4c9e-8ca6-e8c5e72f44a1
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ce9c8b189991e4102fcc9d17b88747d4ce55efec
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570913"
---
# <a name="iattach--imapiprop"></a>IAttach : IMAPIProp

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
保持し、メッセージの添付ファイルのプロパティへのアクセスを提供します。 **IAttach**インターフェイスには、独自の一意のメソッドがありません。 添付ファイルを使用する方法の詳細については、 [MAPI の添付ファイル](mapi-attachments.md)や[添付ファイル テーブル](attachment-tables.md)を参照してください。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|によって公開されます。  <br/> |オブジェクトの添付ファイル  <br/> |
|によって実装されます。  <br/> |メッセージ ストア プロバイダー  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーション  <br/> |
|インターフェイスの識別子。  <br/> |IID_IAttachment  <br/> |
|ポインターの型。  <br/> |LPATTACH  <br/> |
|トランザクション モデル:  <br/> |トランザクション処理  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

このインターフェイスには、固有のメソッドがありません。
  
|**必須のプロパティ**|**Access**|
|:-----|:-----|
|**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_ATTACH_METHOD**([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))  <br/> |値の取得および設定が可能です。  <br/> |
|**PR_RENDERING_POSITION**([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))  <br/> |値の取得および設定が可能です。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI インターフェイス](mapi-interfaces.md)

