---
title: ハイブリッド コマンド (デスクトップ データベース参照のアクセス)
TOCTitle: Hybrid Commands
ms:assetid: 55654274-0494-349f-820d-92108284449d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249286(v=office.15)
ms:contentKeyID: 48544929
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: aa95956fb50a5cd15fa4415e65d4a701f2e48feb
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477949"
---
# <a name="hybrid-commands"></a><span data-ttu-id="dd969-102">ハイブリッド コマンド</span><span class="sxs-lookup"><span data-stu-id="dd969-102">Hybrid Commands</span></span>


<span data-ttu-id="dd969-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="dd969-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="dd969-p101">ハイブリッド コマンドとは、部分的にパラメーター化されたコマンドを指します。次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="dd969-p101">Hybrid commands are partially parameterized commands. For example:</span></span>

```vb 
 
SHAPE {select * from plants} 
 APPEND( {select * from customers where country = ?} 
 RELATE PlantCountry TO PARAMETER 0, 
 PlantRegion TO CustomerRegion ) 
```

<span data-ttu-id="dd969-106">ハイブリッド コマンドのキャッシュ動作は、通常のパラメーター化されたコマンドと同じです。</span><span class="sxs-lookup"><span data-stu-id="dd969-106">The caching behavior for a hybrid command is the same as that of regular parameterized commands.</span></span>

