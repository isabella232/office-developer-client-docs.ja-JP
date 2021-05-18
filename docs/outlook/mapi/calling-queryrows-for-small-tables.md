---
title: 小さなテーブルの QueryRows の呼び出し
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
# <a name="calling-queryrows-for-small-tables"></a>小さなテーブルの QueryRows の呼び出し

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
小さなテーブルから行を取得する場合は、最初に制限を作成する代わりに [IMAPITable::QueryRows](imapitable-queryrows.md) を呼び出します。 制限の作成は、プロバイダーが最初にテーブルを作成し、元のテーブルで一致する行を見つけてから、その行を新しいテーブルにコピーする必要があるため、パフォーマンスに影響します。 テーブル内の行の総数が 100 未満の場合は、すべての行を読み取り [、IMAPITable::FindRow](imapitable-findrow.md) を呼び出して適切な行を見つける方が効果的です。 これは、この情報が時折必要な場合に特に優れた戦略です。 
  
制限を使用する適切な時間は、制限された情報またはフィルター処理された情報が、より長い期間使用される場合、または頻繁に使用される場合です。 たとえば、未読メッセージを含むビューが常に必要な場合は、使用する適切な呼び出しが制限になります。
  

