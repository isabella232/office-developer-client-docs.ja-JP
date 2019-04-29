---
title: 小数値によるテーブルの位置設定
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 80d31611-e508-4b17-b482-bedf76db26ff
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7800a58cad7b4e2b0b1696706c8e1d401ed424d7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437337"
---
# <a name="setting-table-position-with-a-fractional-value"></a>小数値によるテーブルの位置設定

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
Table ユーザーは、合計に対する行のおおよそのパーセンテージを表す位置に移動できます。 この配置方法では、正確な行に移動するのではなく、分数に基づいてテーブルを複数の部分に分割します。 表ユーザーは、たとえば、表の中の半方向の位置、または表の中から7/8 の行に移動することができます。 
  
 **行の概数をカーソルを移動するには**
  
- 呼び出し[IMAPITable:: seekrowapprox](imapitable-seekrowapprox.md) **seekrowapprox**は、テーブルの先頭を基準にして、特定のパーセンテージの行を表す行に移動します。 このパーセンテージは_ulnumerator_パラメーターと_ulnumerator_パラメーターで指定されています。 **seekrowapprox**は、スクロールバーを実装するためによく使用されます。 
    
 **表のおおよその位置を確認するには**
  
- 呼び出し[IMAPITable:: queryposition](imapitable-queryposition.md)。 **queryposition**は、現在の位置をユーザーに通知するために使用できます。 表の行数と現在の行の数に基づいて、小数値を設定します。 この値は近似値を表すものと想定します。 表の実装では、厳密な実装は、特に、カテゴリ化されたテーブルでは、正確に実装するのにコストがかかるため、正確な位置を計算しないことをお勧め 
    
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

