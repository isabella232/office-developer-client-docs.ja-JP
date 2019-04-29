---
title: ブックマークによるテーブルの位置設定
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 56ab37f9-5aa6-4e9d-9dc8-b3d95aa19f35
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f0b041cecca92c0ced32631c67c72fcafdab2a16
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422461"
---
# <a name="setting-a-table-position-with-a-bookmark"></a>ブックマークによるテーブルの位置設定

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ブックマークは、テーブル内の特定の位置を示すリソースです。 ブックマークを設定すると、後で位置に戻ることができるようになります。この機能を使用すると、テーブル操作のパフォーマンスを大幅に向上させることができます。 MAPI は、3つの標準のブックマークを定義します。 
  
|||
|:-----|:-----|
|BOOKMARK_CURRENT  <br/> |表の現在の行を指します。  <br/> |
|BOOKMARK_BEGINNING  <br/> |表の最初の行を指します。  <br/> |
|BOOKMARK_END  <br/> |表の最後の行を指します。  <br/> |
   
表の実装者は、これらの標準のブックマークをサポートする必要があります。また、他のユーザーをサポートすることもできます。 ただし、ブックマークはリソースで、リソースは限られているので、ブックマークユーザーはできるだけ早く解放する必要があります。 
  
 **現在の表の位置にブックマークを設定するには**
  
- Call [IMAPITable:: createbookmark](imapitable-createbookmark.md) 場合によっては、新しいブックマークの割り当てに使用できるメモリが不足することがあり、 **createbookmark**が MAPI_E_UNABLE_TO_COMPLETE エラー値を返します。 
    
 **ブックマークを解放するには**
  
- 関数 Call [IMAPITable:: freebookmark](imapitable-freebookmark.md)。
    
 **ブックマーク位置にカーソルを移動するには**
  
- Call [IMAPITable:: seekrow](imapitable-seekrow.md)。 **seekrow**は BOOKMARK_CURRENT position の新しい値を確立します。 **seekrow**を使用すると、たとえばテーブルを現在の位置から10行分移動したり、先頭からやり直すことができます。 クライアントまたはサービスプロバイダーは、テーブルのカレント、先頭、または末尾、あるいは定義済みのブックマークに関連付けられているその他の位置までシークできます。 前方または後方のどちらかの方向に移動し、操作を指定した行数に制限できます。 原則として、発信者は**seekrow**で50行以内をシークする必要があります。[IMAPITable:: seekrowapprox](imapitable-seekrowapprox.md)は、より多くの行で使用する必要があります。 
    
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

