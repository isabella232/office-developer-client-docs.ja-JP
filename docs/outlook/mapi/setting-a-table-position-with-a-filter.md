---
title: フィルターによるテーブルの位置設定
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0d66124b-a018-4db4-b55b-a0e5ed467e14
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6b21d6746baf438af438787d966d9af886d4a74f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316045"
---
# <a name="setting-a-table-position-with-a-filter"></a>フィルターによるテーブルの位置設定

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
Table ユーザーは、フィルタ条件のセットに一致する行にカーソルを移動することができます。 フィルターは、列のプロパティ値、ビットマスク、サブオブジェクトなど、さまざまなガイドラインに基づいて行うことができます。 フィルターは、 [srestriction](srestriction.md)構造を使用して MAPI で指定されます。 
  
 **制限で設定された条件に一致する最初の行にテーブルを配置するには**
  
- [IMAPITable:: FindRow](imapitable-findrow.md)メソッドを呼び出します。 **FindRow**は、特定のブックマークで表される行から順に検索し、制限で指定された条件に一致する行を検索します。 **FindRow**は、小数点以下の値ではなく、文字列に基づくスクロールバーを実装するのに便利です。 たとえば、クライアントは、統合されたアドレス帳を検索するときに、MAPI の**FindRow**の実装を呼び出すことができます。これにより、ユーザーは1つ以上の文字を入力して、指定した文字で始まる最初の名前を検索できます。 
    
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

