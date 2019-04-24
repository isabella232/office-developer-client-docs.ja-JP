---
title: iattach imapiprop
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
ms.openlocfilehash: 2ef3bc973e12bd5630cc00b3c512b748d4a16e86
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341623"
---
# <a name="iattach--imapiprop"></a>IAttach : IMAPIProp

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ内の添付ファイルのプロパティへのアクセスを保持および提供します。 **iattach**インターフェイスには、独自の独自のメソッドはありません。 添付ファイルの使用方法の詳細については、「 [MAPI 添付](mapi-attachments.md)ファイルと[添付ファイルの表](attachment-tables.md)」を参照してください。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|公開者:  <br/> |Attachment オブジェクト  <br/> |
|実装元:  <br/> |メッセージストアプロバイダー  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーション  <br/> |
|インターフェイス識別子:  <br/> |IID_IAttachment  <br/> |
|ポインターの種類:  <br/> |lpattach  <br/> |
|トランザクションモデル:  <br/> |一括  <br/> |
   
## <a name="vtable-order"></a>v の順序

このインターフェイスには一意のメソッドはありません。
  
|**必須のプロパティ**|**Access**|
|:-----|:-----|
|**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_ATTACH_METHOD**([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))  <br/> |読み取り/書き込み  <br/> |
|**PR_RENDERING_POSITION**([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))  <br/> |読み取り/書き込み  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

