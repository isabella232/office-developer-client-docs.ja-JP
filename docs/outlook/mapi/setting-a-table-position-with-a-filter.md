---
title: フィルターによるテーブルの位置設定
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0d66124b-a018-4db4-b55b-a0e5ed467e14
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 6c4db9c67fc712143657fe66b86ea33ef2b9c272
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565593"
---
# <a name="setting-a-table-position-with-a-filter"></a>フィルターによるテーブルの位置設定

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
テーブルのユーザーは、一連のフィルター条件に一致する行にカーソルを移動できます。 フィルターは、さまざまな列プロパティの値やビットマスク、サブオブジェクトなどのガイドラインに基づいていることができます。 [SRestriction](srestriction.md)構造体を使用して MAPI では、フィルターが指定されています。 
  
 **制限の中で確立された条件に一致する最初の行に表を配置するには**
  
- [IMAPITable::FindRow](imapitable-findrow.md)メソッドを呼び出します。 **FindRow**は特定のブックマークで表される行から始めて、前方または後方のいずれかの方向の制限で指定された条件に一致するローを検索します検索します。 **FindRow**は、小数部の値ではなく、文字の文字列に基づくスクロール バーを実装するために役立ちます。 などの指定された文字で始まる最初の名前を検索するのには、1 つまたは複数の文字を入力することにより、ユーザーを有効にする統合されたアドレス帳から検索する場合、クライアントは**FindRow**の MAPI の実装を呼び出すことができます。 
    
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

