---
title: テーブルを操作するためのヒント
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: adb4d589-7e03-4222-8717-898ef397c6b6
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 451bab57d4e2e8669a25d119f9ce28a8f78e628f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804099"
---
# <a name="tips-for-working-with-tables"></a>テーブルを操作するためのヒント

  
  
**適用されます**: Outlook 
  
MAPI を使用するテーブルは、リレーショナル データベースのテーブルに like 作業を少しです。 ユーザーは、ビューの行と列の数を制限し、それらの順序を指定できます。 行には、同時にまたはグループで、取得した 1 つをすることができます。 カーソルの現在位置を追跡するテーブル内の特定の場所に移動できます。 
  
テーブルを使用するクライアント インターフェイスを使用して、読み取り専用、 [IMAPITable: IUnknown](imapitableiunknown.md)テーブルの基になっているデータを所有するかどうかによって、サービス プロバイダーが**IMAPITable**をいずれかを使用できますが、または[ITableData: IUnknown](itabledataiunknown.md)。 テーブルのすべてのユーザーか、または呼び出すことができる操作と広く使用されていないためより高度な操作としては、これらのインタ フェースで定義されている操作を分類できます。 いくつかの高度な操作は、単純に実装します。他のユーザーは複雑、ですが、ごく一部の MAPI コンポーネントに関係の。 
  
一般的な操作は次のとおりです。
  
- 列の操作、1 つの列に影響を与えます。 列セットと、それらを含めるように順序に含まれるプロパティを指定することが含まれます。
    
- 行操作には、単一行に影響します。 データの取得と保守作業が含まれます: 追加、削除、および 1 つの行または行を変更します。
    
- グローバル操作、テーブル全体に影響します。 イベント通知、検索および並べ替えが含まれます。
    
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)
