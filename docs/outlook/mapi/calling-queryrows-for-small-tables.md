---
title: 小さなテーブルに対する QueryRows の呼び出し
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8c38bb0f-de0b-4d70-9f6d-db652445e137
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 8b38dcc485e75f94ccf4f4c3c8c9a57d314465a6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404177"
---
# <a name="calling-queryrows-for-small-tables"></a>小さなテーブルに対する QueryRows の呼び出し

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
小さなテーブルから行を取得するときは、最初に制限を作成するのではなく、 [IMAPITable:: QueryRows](imapitable-queryrows.md)を呼び出します。 プロバイダーが最初にテーブルを作成し、その後、元のテーブルで一致する行を見つけて、その行を新しいテーブルにコピーする必要があるため、制限の作成はパフォーマンスに影響します。 表の行数の合計が100よりも低い場合は、すべての行を読み取ってから、 [IMAPITable:: FindRow](imapitable-findrow.md)を呼び出して適切な行を検索する方が効率がよいでしょう。 これは、この情報がたまにしか必要ない場合に特に適した戦略です。 
  
制限を適切に使用するには、制限またはフィルター処理された情報を長期間にわたって使用したり、頻繁に使用したりすることが適切な時間です。 たとえば、未読メッセージがあるビューが常に必要な場合は、適切な呼び出しを使用するように制限を行います。
  

