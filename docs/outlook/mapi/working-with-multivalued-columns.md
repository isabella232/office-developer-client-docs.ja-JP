---
title: 複数値列の操作
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 911a41c3-c10f-4473-8853-fafb56b721ba
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 78f6083cf17bb21152df1a7ea09825f3be7f0e37
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572943"
---
# <a name="working-with-multivalued-columns"></a>複数値列の操作

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
複数値の列には、1 つの値ではなく基本データ型の値の配列を含むプロパティは、複数値を持つプロパティのデータが含まれています。 テーブルの [なし] は、複数値を持つプロパティの既定の列セットであるため、テーブルのユーザーが要求した場合のみ複数値を持つプロパティがテーブルに含まれます。 
  
複数値を持つ列は、テーブルに表示できます。
  
- 1 つの行、列の 1 つのインスタンスに表示されるプロパティ値のすべてです。 これは、既定値です。
    
    - または、
    
- 一連の行のプロパティ値ごとに 1 行にします。 そこに多数の行は、複数値を持つプロパティの値とする、そこに独自の行の列にそれぞれ一意の値が表示されます。 各行では、 **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) プロパティでは、一意の値ですが、ほかの列と同じ値を持ちます。 行に複数値を持つ 2 つ以上の列が含まれている場合たとえば、 _M_と_N_の 2 つの列それぞれ値は、[ _M\*N_テーブルの行のインスタンスが表示されます。 
    
テーブルのユーザーは、メソッドを呼び出して、 [IMAPITable::SetColumns](imapitable-setcolumns.md) MVI_FLAG フラグが設定されている複数値の列のプロパティの型での表示の既定値以外の種類を要求します。 MVI_FLAG フラグは、論理**OR**演算と MV_FLAG と MV_INSTANCE のフラグを組み合わせることの結果として定義されている定数です。 **SetColumns**で使用されているだけでなく MVI_FLAG 渡すこともできます[IMAPITable::SortTable](imapitable-sorttable.md)に、 _lpSortCriteria_パラメーターと[IMAPITable::Restrict](imapitable-restrict.md)の_lpRestriction_の**ulPropTag**のメンバーでパラメーターです。 渡されると、MVI_FLAG、 **SortTable**は**SetColumns**、複数値を持つ列の値ごとに 1 つの行を追加して、インスタンス内の単一の値で並べ替えを同様に実行します。 値ごとに 1 つの行が追加されます。 
  
 **だけに制限する**、ただし、展開されない複数値を持つ列計算行にします。 MVI_FLAG セットを使用して複数値を持つ列は、テーブルを制限することでその列を使用するサービス プロバイダーに指示します。 制約のプロパティの値がある場合と同じように列の[IMAPITable::QueryRows](imapitable-queryrows.md)によって返される単一値プロパティ タグがあります。 
  
テーブルの実装側では、既定の表示の種類をサポートするために必要なだけと、呼び出し元が他の選択を要求すると、MAPI_E_TOO_COMPLEX の値を返すことができます。 両方の種類の表示をサポートする機能は、メッセージ ストア プロバイダーがフォルダーの内容テーブルを実装するために最も重要です。 
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

