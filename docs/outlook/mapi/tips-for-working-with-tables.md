---
title: ヒント操作の詳細
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: adb4d589-7e03-4222-8717-898ef397c6b6
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 8f310c6331df941d3093b276b6dec47f740412e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439738"
---
# <a name="tips-for-working-with-tables"></a>ヒント操作の詳細

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI テーブルの操作は、リレーショナル データベース テーブルの操作と少し似たものになります。 ユーザーは、ビュー内の行と列の数を制限し、その順序を指定できます。 行は、一度に 1 つ、またはグループで取得できます。 現在の位置を追跡するカーソルは、テーブル内の特定の場所に移動できます。 
  
テーブルを使用するには、クライアントは読み取り専用インターフェイス [IMAPITable : IUnknown](imapitableiunknown.md)を使用しますが、サービス プロバイダーは、テーブルが基づくデータを所有するかどうかに応じて **、IMAPITable** または [ITableData : IUnknown](itabledataiunknown.md)を使用できます。 これらのインターフェイスで定義された操作は、テーブルのすべてのユーザーが実行または呼び出す操作、および高度な操作が行われるため、広く使用されていない操作として分類できます。 高度な操作の中には、実装が複雑な操作があります。他のコンポーネントは複雑ではなく、MAPI コンポーネントの少数派に関心があります。 
  
より一般的な操作は次のとおりです。
  
- 1 つの列に影響する列操作。 これには、列セットに含めるプロパティと、列セットを含める順序の指定が含まれます。
    
- 1 つの行に影響する行操作。 これには、データ取得とメンテナンス操作 (1 行または 1 行の追加、削除、変更) が含まれます。
    
- テーブル全体に影響を与えるグローバル操作。 これには、イベント通知、検索、並べ替えが含まれます。
    
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

