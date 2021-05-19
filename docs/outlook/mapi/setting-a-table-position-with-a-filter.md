---
title: フィルターを使用してテーブルの位置を設定する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0d66124b-a018-4db4-b55b-a0e5ed467e14
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6b21d6746baf438af438787d966d9af886d4a74f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425471"
---
# <a name="setting-a-table-position-with-a-filter"></a>フィルターを使用してテーブルの位置を設定する

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
テーブル ユーザーは、一連のフィルター条件に一致する行にカーソルを移動できます。 フィルターは、列のプロパティ値、ビットマスク、サブオブジェクトなど、さまざまなガイドラインに基づいて設定できます。 フィルターは [、SRestriction 構造を使用して MAPI で指定](srestriction.md) されます。 
  
 **制限で設定された条件に一致する最初の行にテーブルを配置するには**
  
- [IMAPITable::FindRow メソッドを呼び出](imapitable-findrow.md)します。 FindRow は、特定のブックマークで表される行から順方向または後方方向に検索し、制限で指定された条件に一致する行を検索します。 **FindRow** は、小数部の値ではなく、文字列に基づくスクロール バーを実装する場合に便利です。 たとえば、クライアントは、統合アドレス帳を検索するときに MAPI の **FindRow** の実装を呼び出して、1 つ以上の文字を入力して、指定された文字で始まる最初の名前を見つけるために、ユーザーを有効にできます。 
    
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

