---
title: 小さなテーブルのスプーラーを呼び出す
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8c38bb0f-de0b-4d70-9f6d-db652445e137
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 40533470681182719f5009b048e3b173b92ef290
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799744"
---
# <a name="calling-queryrows-for-small-tables"></a>小さなテーブルのスプーラーを呼び出す

  
  
**適用されます**: Outlook 
  
小さなテーブルから行を検索する場合は、最初に制約を作成する代わりに[IMAPITable::QueryRows](imapitable-queryrows.md)を呼び出します。 制限、パフォーマンスに与える影響を作成するは、プロバイダーがテーブルをまず作成する必要がありますので、元のテーブルに一致する行を検索し、新しいテーブルに行をコピーします。 テーブル内の行の合計数が 100 未満の場合は、すべての行を読み取るし、該当する行を見つけるには、 [IMAPITable::FindRow](imapitable-findrow.md)を呼び出すにはより効果的な可能性があります。 これは、この情報が常時必要な場合に特に効果的な戦略です。 
  
制限を使用する適切な時間は、制限またはフィルタ リングされた情報が長い期間にわたって使用されるか、頻繁に使用されるときです。 未読のメッセージでは、ビューが常に必要がある場合、この制限は適切な呼び出しを使用するになります。
  

