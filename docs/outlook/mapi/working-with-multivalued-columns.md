---
title: 複数値の列の操作
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 911a41c3-c10f-4473-8853-fafb56b721ba
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 34f19e279c86e0c0856d242cf2aa13d744d46f13
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420186"
---
# <a name="working-with-multivalued-columns"></a>複数値の列の操作

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
複数値の列には、複数値プロパティのデータが含まれます。これは、1 つの値ではなく、基本型の値の配列を持つプロパティです。 既定の列セットには複数値プロパティが含まれているテーブルはないので、テーブルのユーザーが要求した場合にのみ、複数値プロパティがテーブルに含まれます。 
  
複数値の列は、次の表に表示できます。
  
- 1 つの行で、すべてのプロパティ値が 1 つの列インスタンスに表示されます。 これが既定です。
    
    - Or -
    
- 一連の行で、プロパティ値ごとに 1 行を指定します。 各一意の値は、複数値プロパティの値と同じ数の行を持つ、独自の行の列に表示されます。 各行には、PR_INSTANCE_KEY **(** [PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) プロパティの一意の値がありますが、他の列の値は同じです。 複数の値を持つ複数の列が 1 つの行に含まれている場合 (たとえば、  _それぞれ M_ 値と N 値を持つ 2 つの列)、行の  _M_  _\* N_ インスタンスがテーブルに表示されます。 
    
テーブル ユーザーは、複数値列のプロパティの種類で MVI_FLAG フラグが設定された [IMAPITable::SetColumns](imapitable-setcolumns.md) メソッドを呼び出すことによって、既定以外の種類の表示を要求します。 このMVI_FLAGフラグは、論理 OR 操作と MV_FLAGとMV_INSTANCEの組み合わせの結果として定義される **定数** です。 **SetColumns** で使用されるだけでなく、MVI_FLAG は _lpSortCriteria_ パラメーターの [IMAPITable::SortTable、lpRestriction](imapitable-sorttable.md)パラメーターの **ulPropTag** メンバーでは [IMAPITable::Restrict](imapitable-restrict.md)にも渡されます。  MVI_FLAG を渡した場合 **、SortTable** は **SetColumns** と同様に実行され、複数値列の値ごとに 1 行を追加し、インスタンス内の 1 つの値で並べ替えを行います。 値ごとに 1 つの行が追加されます。 
  
 **ただし**、複数値の列を追加の計算行に展開することはできません。 複数値を持つ列MVI_FLAG、サービス プロバイダーは、その列を使用してテーブルを制限するように指示します。 制限にプロパティ値がある場合は、列の [IMAPITable::QueryRows](imapitable-queryrows.md) によって返されるプロパティ タグと同じ 1 つの値プロパティ タグである必要があります。 
  
テーブルの実装者は、既定の種類の表示をサポートするためにのみ必要であり、呼び出し元が他の選択肢を要求MAPI_E_TOO_COMPLEXの値を返すことができます。 両方の種類の表示をサポートする機能は、フォルダー コンテンツ テーブルを実装するメッセージ ストア プロバイダーにとって最も重要です。 
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

