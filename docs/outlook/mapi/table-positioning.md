---
title: 表の配置
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a0cbbc93-8074-4e86-b660-ee7bab910587
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 656f696c58e9b62e7e601d7f531870b8c385e862
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345655"
---
# <a name="table-positioning"></a><span data-ttu-id="c1390-103">表の配置</span><span class="sxs-lookup"><span data-stu-id="c1390-103">Table Positioning</span></span>

  
  
<span data-ttu-id="c1390-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1390-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1390-105">テーブル内の現在の位置は、常にカーソルで示されます。</span><span class="sxs-lookup"><span data-stu-id="c1390-105">The current position within a table is always indicated by a cursor.</span></span> <span data-ttu-id="c1390-106">テーブルのビューごとに1つのカーソルがあります。この値は、テーブルの実装によって設定されます。</span><span class="sxs-lookup"><span data-stu-id="c1390-106">There is one cursor for each view of a table; its value is set by the table's implementer.</span></span> <span data-ttu-id="c1390-107">テーブルを使用するクライアントまたはサービスプロバイダーがテーブルの位置を変更する呼び出しを行う場合、カーソルの値はリセットされます。</span><span class="sxs-lookup"><span data-stu-id="c1390-107">When a client or service provider using the table makes a call to change the position of the table, the value of the cursor is reset.</span></span> <span data-ttu-id="c1390-108">テーブルの位置は、次のように変更できます。</span><span class="sxs-lookup"><span data-stu-id="c1390-108">A table's position can be changed with:</span></span>
  
- <span data-ttu-id="c1390-109">ブックマーク</span><span class="sxs-lookup"><span data-stu-id="c1390-109">A bookmark.</span></span>
    
- <span data-ttu-id="c1390-110">小数値。</span><span class="sxs-lookup"><span data-stu-id="c1390-110">A fractional value.</span></span>
    
- <span data-ttu-id="c1390-111">フィルター。</span><span class="sxs-lookup"><span data-stu-id="c1390-111">A filter.</span></span>
    

