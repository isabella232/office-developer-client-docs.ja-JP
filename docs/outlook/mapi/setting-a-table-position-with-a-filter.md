---
title: フィルターを使用してテーブルの位置を設定します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0d66124b-a018-4db4-b55b-a0e5ed467e14
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 4c3a5c13433fb2f037be24ddd4c877579429f7bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803892"
---
# <a name="setting-a-table-position-with-a-filter"></a>フィルターを使用してテーブルの位置を設定します。

  
  
**適用されます**: Outlook 
  
テーブルのユーザーは、一連のフィルター条件に一致する行にカーソルを移動できます。 フィルターは、さまざまな列プロパティの値やビットマスク、サブオブジェクトなどのガイドラインに基づいていることができます。 [SRestriction](srestriction.md)構造体を使用して MAPI では、フィルターが指定されています。 
  
 **制限の中で確立された条件に一致する最初の行に表を配置するには**
  
- [IMAPITable::FindRow](imapitable-findrow.md)メソッドを呼び出します。 **FindRow**は特定のブックマークで表される行から始めて、前方または後方のいずれかの方向の制限で指定された条件に一致するローを検索します検索します。 **FindRow**は、小数部の値ではなく、文字の文字列に基づくスクロール バーを実装するために役立ちます。 などの指定された文字で始まる最初の名前を検索するのには、1 つまたは複数の文字を入力することにより、ユーザーを有効にする統合されたアドレス帳から検索する場合、クライアントは**FindRow**の MAPI の実装を呼び出すことができます。 
    
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

