---
title: 小数部の値を使用してテーブルの位置を設定する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 80d31611-e508-4b17-b482-bedf76db26ff
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b22cefe52bf525f31041dcf87c94a0c32751c5a3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550044"
---
# <a name="setting-table-position-with-a-fractional-value"></a>小数部の値を使用してテーブルの位置を設定する

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
テーブル ユーザーは、合計に対する行のおよその割合を表す位置に移動できます。 正確な行に移動するのではなく、この配置方法では、表を分数に基づいて部分に分割します。 テーブル ユーザーは、たとえば、テーブルの中途半端なポイントに移動したり、テーブルの 7/8 の行に移動できます。 
  
 **カーソルを移動するには、およその行数**
  
- [IMAPITable::SeekRowApprox を呼び出します](imapitable-seekrowapprox.md)。 **SeekRowApprox は** 、表の先頭に関連する行の特定の割合を表す行に移動します。 このパーセンテージは  _、ulNumerator パラメーター_ と  _ulDenominator パラメーターで指定_ されます。 **SeekRowApprox は、** スクロール バーを実装するために頻繁に使用されます。 
    
 **テーブルのおおよその位置を決定するには**
  
- [IMAPITable::QueryPosition を呼び出します](imapitable-queryposition.md)。 **QueryPosition** を使用して、現在の位置をユーザーに通知できます。 テーブル内の行数と現在の行の数に基づいて小数部の値を設定します。 この値が近似値を表す必要があります。 正確な実装は、特に分類されたテーブルでは、呼び出すのにコストがかかる可能性があるため、テーブル実装者は正確な位置を計算しないのでお勧めしています。 
    
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

