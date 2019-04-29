---
title: 複数値列の処理
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
# <a name="working-with-multivalued-columns"></a>複数値列の処理

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
複数値列には複数値プロパティのデータが含まれています。これは、単一値の代わりに基本型の値の配列を持つプロパティです。 既定の列セットに複数値プロパティが含まれていないテーブルがあるので、テーブルのユーザーがテーブルを要求した場合にのみ、複数値プロパティがテーブルに含まれます。 
  
複数値列をテーブルに表示できます。
  
- 1つの行で、すべてのプロパティ値が1つの列のインスタンスに表示されます。 これは既定値です。
    
    - や
    
- 一連の行で、各プロパティ値に1つの行が含まれます。 それぞれの一意の値は、1つの列にそれぞれの行に表示され、複数値プロパティに値があるとしても行数が多くなります。 各行には、 **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) プロパティの一意の値がありますが、その他の列には同じ値があります。 1つの行に複数の値を持つ複数の列が含まれている場合、たとえば、2つの列にそれぞれ_m_と_N_の値がある場合、テーブルにはその行の_\*M N 個_のインスタンスが表示されます。 
    
複数値列のプロパティの種類で、MVI_FLAG フラグを設定して[IMAPITable:: SetColumns](imapitable-setcolumns.md)メソッドを呼び出すことにより、table ユーザーが既定以外の種類の表示を要求します。 MVI_FLAG フラグは、MV_FLAG と MV_INSTANCE のフラグを論理**OR**演算で結合した結果として定義される定数です。 SetColumns で使用されているだけでなく、MVI_FLAG [](imapitable-restrict.md)を**** の_lp:_ : [sorttable](imapitable-sorttable.md)に渡すこともできます。このパラメーターには、 _lpRestriction_の**ulPropTag**メンバーを指定します。parameter. MVI_FLAG を通過すると、 **sorttable**は**SetColumns**に対して同様に実行し、複数値列の値ごとに1つの行を追加し、インスタンスの単一の値を並べ替えます。 値ごとに1つの行が追加されます。 
  
 ただし、[**制限**] では、複数値列が他の計算行に展開されることはありません。 MVI_FLAG セットを持つ複数値列は、この列を使用してテーブルを制限することをサービスプロバイダーに指示します。 制限内にプロパティ値がある場合、その値は、列に対して[IMAPITable:: QueryRows](imapitable-queryrows.md)によって返される1つの値のプロパティタグと同一である必要があります。 
  
表実装者は、既定の種類の表示をサポートするためにのみ必要であり、発信者が他の方法を要求したときに MAPI_E_TOO_COMPLEX 値を返すことができます。 両方の種類の表示をサポートする機能は、フォルダーコンテンツテーブルを実装するメッセージストアプロバイダーにとって最も重要です。 
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

