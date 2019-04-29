---
title: テーブルを使用するためのヒント
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
# <a name="tips-for-working-with-tables"></a>テーブルを使用するためのヒント

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI テーブルを使用することは、リレーショナルデータベーステーブルを処理するのと似ています。 ユーザーは、ビュー内の行数と列数を制限し、その順序を指定できます。 行は、一度に1つまたは複数のグループで取得できます。 現在の位置を追跡するカーソルは、テーブルの特定の位置に移動することができます。 
  
テーブルを使用する場合、クライアントは、サービスプロバイダーとして、テーブルの基になるデータを所有しているかどうかに応じて、読み取り専用のインターフェイス、 **** [IMAPITable: iunknown](imapitableiunknown.md)を使用します。 [](itabledataiunknown.md) これらのインターフェイスで定義されている操作は、テーブルのすべてのユーザーが、より高度な処理を実行したり、頻繁に使用されていない操作を実行したりできる操作として分類できます。 高度な操作の一部は、実装が複雑になります。他のユーザーは複雑ではありませんが、少数の MAPI コンポーネントに関連しています。 
  
一般的な操作は次のとおりです。
  
- 列の操作。単一の列に影響します。 これには、列セットに含めるプロパティと、それらを含める順序を指定することが含まれます。
    
- 行の操作。1つの行に影響します。 これには、データの取得とメンテナンス操作が含まれます。これには、1つの行または行の追加、削除、および変更があります。
    
- テーブル全体に影響を与えるグローバル操作。 これらには、イベント通知、検索、並べ替えが含まれます。
    
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

