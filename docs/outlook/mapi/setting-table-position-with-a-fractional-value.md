---
title: 小数値によるテーブルの位置設定
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 80d31611-e508-4b17-b482-bedf76db26ff
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 104de38a41408091a6fbb69995de4f41f6fea6a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803894"
---
# <a name="setting-table-position-with-a-fractional-value"></a>小数値によるテーブルの位置設定

  
  
**適用対象**: Outlook 
  
テーブルのユーザーは、合計を基準にして行のおおよその割合を表す位置に移動できます。 行を正確に移動するのではなく分割を配置するのには、このメソッドの部分にテーブルに基づく分数。 テーブルのユーザーは、テーブルの半分のポイントに、またはテーブルを使用する方法の 7/8 の行に移動できます。 
  
 **カーソル行のおおよその数を移動するには**
  
- [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md)を呼び出します。 **SeekRowApprox**は、テーブルの先頭を基準にして行の特定のパーセントを表す行に移動します。 この割合は、 _ulNumerator_および_ulDenominator_パラメーターで指定されます。 **SeekRowApprox**は、スクロール バーを実装するために頻繁に使用されます。 
    
 **テーブルのおおよその位置を決定するには**
  
- [IMAPITable::QueryPosition](imapitable-queryposition.md)を呼び出します。 **QueryPosition**は、ユーザーの現在位置を通知するために使用できます。 小数部の値がテーブル内の行の数および現在の行の数に基づいて設定します。 この値が近似値を表すことを期待します。 テーブルの実装側は、正確な実装を呼び出すには、分類されたテーブルでは特に高価なことができるため、正確な位置を計算していないことをお勧めします。 
    
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

