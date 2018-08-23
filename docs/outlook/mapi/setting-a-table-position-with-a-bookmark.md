---
title: ブックマークによるテーブルの位置設定
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 56ab37f9-5aa6-4e9d-9dc8-b3d95aa19f35
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d53f15cb439494ae99ff45509ed14c0928756d8f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803887"
---
# <a name="setting-a-table-position-with-a-bookmark"></a>ブックマークによるテーブルの位置設定

  
  
**適用対象**: Outlook 
  
ブックマークは、テーブル内の特定の場所を示すリソースです。 ブックマークの設定は、後で、テーブルの操作のパフォーマンスを大幅に向上する機能の状態に戻します。 MAPI には、標準的な 3 つのブックマークが定義されています。 
  
|||
|:-----|:-----|
|BOOKMARK_CURRENT  <br/> |テーブルの現在の行へのポインター。  <br/> |
|BOOKMARK_BEGINNING  <br/> |テーブルの最初の行へのポインター。  <br/> |
|BOOKMARK_END  <br/> |テーブルの最後の行をポイントします。  <br/> |
   
テーブルの実装は、これらの標準的なブックマークをサポートする必要し、も他のユーザーをサポートできます。 ただし、ブックマークは、リソースをリソースが限られたため、ブックマークのユーザーがそれらを解放、できるだけ早く。 
  
 **テーブルの現在の位置にブックマークを設定するのには**
  
- [IMAPITable::CreateBookmark](imapitable-createbookmark.md)を呼び出します。 場合によってはメモリ不足の原因で MAPI_E_UNABLE_TO_COMPLETE のエラー値を返す**CreateBookmark** 、新しいブックマークを割り当てることがあります。 
    
 **ブックマークを解放するには**
  
- [IMAPITable::FreeBookmark](imapitable-freebookmark.md)を呼び出します。
    
 **ブックマークが設定された位置にカーソルを移動するのには**
  
- [IMAPITable::SeekRow](imapitable-seekrow.md)を呼び出します。 **SeekRow**は、BOOKMARK_CURRENT の位置の新しい値を設定します。 **SeekRow**使用できます、たとえば、現在の位置から 10 個のテーブルの行を配置する、または先頭に最初からやり直す。 クライアントまたはサービス プロバイダー以降では、現在、検索したり、最後のテーブル、または定義済みのブックマークに関連付けられている他の任意の位置。 順方向または逆方向と操作の制限のいずれかで指定された行数に移動できます。 原則として呼び出し元の**SeekRow**; で 50 文字以下の行をシークする必要があります。[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md)は、多数の行を使用してください。 
    
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

