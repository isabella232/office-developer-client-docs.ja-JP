---
title: ブックマークを使用してテーブルの位置を設定する
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
# <a name="setting-a-table-position-with-a-bookmark"></a>ブックマークを使用してテーブルの位置を設定する

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ブックマークは、テーブル内の特定の場所を示すリソースです。 ブックマークを設定すると、後で位置に戻り、テーブル操作のパフォーマンスを大幅に向上させる機能を使用できます。 MAPI では、次の 3 つの標準ブックマークを定義します。 
  
|||
|:-----|:-----|
|BOOKMARK_CURRENT  <br/> |テーブル内の現在の行をポイントします。  <br/> |
|BOOKMARK_BEGINNING  <br/> |テーブルの最初の行をポイントします。  <br/> |
|BOOKMARK_END  <br/> |テーブルの最後の行をポイントします。  <br/> |
   
テーブル実装者は、これらの標準ブックマークをサポートするために必要であり、他のユーザーもサポートできます。 ただし、ブックマークはリソースであり、リソースは限られているため、ブックマーク ユーザーはできるだけ早く解放する必要があります。 
  
 **現在のテーブル位置にブックマークを設定するには**
  
- [IMAPITable::CreateBookmark を呼び出します](imapitable-createbookmark.md)。 新しいブックマークを割り当てるのに十分なメモリが不足し **、CreateBookmark** がエラー値を返MAPI_E_UNABLE_TO_COMPLETE場合があります。 
    
 **ブックマークを解放するには**
  
- [IMAPITable::FreeBookmark を呼び出します](imapitable-freebookmark.md)。
    
 **カーソルをブックマーク位置に移動するには**
  
- [IMAPITable::SeekRow を呼び出します](imapitable-seekrow.md)。 **SeekRow は** 、ユーザーの位置に新しい値BOOKMARK_CURRENTします。 **SeekRow** を使用すると、たとえば、現在の位置から 10 行のテーブルを配置したり、先頭から最初に行を開始したりできます。 クライアントまたはサービス プロバイダーは、テーブルの現在、開始、または終了、または定義済みのブックマークに関連付けられているその他の位置をシークできます。 順方向または後方方向に移動し、操作を指定した行数に制限できます。 原則として、発信者は SeekRow を使用して 50 行以下を **シークする必要があります**。 [IMAPITable::SeekRowApprox は](imapitable-seekrowapprox.md) 、より多くの行で使用する必要があります。 
    
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

