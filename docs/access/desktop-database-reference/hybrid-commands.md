---
title: ハイブリッドコマンド (Access デスクトップデータベースリファレンス)
TOCTitle: Hybrid commands
ms:assetid: 55654274-0494-349f-820d-92108284449d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249286(v=office.15)
ms:contentKeyID: 48544929
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7fe3e6d0afbba82cacd5a55c630f1ca41f3e318a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291909"
---
# <a name="hybrid-commands"></a><span data-ttu-id="deede-102">ハイブリッド コマンド</span><span class="sxs-lookup"><span data-stu-id="deede-102">Hybrid commands</span></span>


<span data-ttu-id="deede-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="deede-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="deede-p101">ハイブリッド コマンドとは、部分的にパラメーター化されたコマンドを指します。次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="deede-p101">Hybrid commands are partially parameterized commands. For example:</span></span>

```vb 
 
SHAPE {select * from plants} 
 APPEND( {select * from customers where country = ?} 
 RELATE PlantCountry TO PARAMETER 0, 
 PlantRegion TO CustomerRegion ) 
```

<span data-ttu-id="deede-106">ハイブリッド コマンドのキャッシュ動作は、通常のパラメーター化されたコマンドと同じです。</span><span class="sxs-lookup"><span data-stu-id="deede-106">The caching behavior for a hybrid command is the same as that of regular parameterized commands.</span></span>

