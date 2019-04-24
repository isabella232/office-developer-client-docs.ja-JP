---
title: 孫の集計
TOCTitle: Grandchild aggregates
ms:assetid: ea5e2e1f-f3d5-f851-623a-a5d1385fe206
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250188(v=office.15)
ms:contentKeyID: 48548462
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a4c50898626488f909616977c6bb50c936434563
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292147"
---
# <a name="grandchild-aggregates"></a><span data-ttu-id="b622d-102">孫の集計</span><span class="sxs-lookup"><span data-stu-id="b622d-102">Grandchild aggregates</span></span>


<span data-ttu-id="b622d-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="b622d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b622d-104">shape コマンドの句で作成されたチャプター列には、(通常は as キーワードを使用して)*チャプターエイリアス名*を指定できます。</span><span class="sxs-lookup"><span data-stu-id="b622d-104">The chapter column created in a clause of a shape command may be given a *chapter-alias name* (typically with the AS keyword).</span></span> <span data-ttu-id="b622d-105">シェイプされた**Recordset**の任意のチャプター内の列は、その列が含まれている子を識別する完全修飾名で識別できます。</span><span class="sxs-lookup"><span data-stu-id="b622d-105">You may identify any column in any chapter of the shaped **Recordset** with a fully qualified name identifying the child containing the column.</span></span> <span data-ttu-id="b622d-106">たとえば、親チャプター chap1 が含まれている場合は、chap2 という子チャプターが含まれているとします。これには、金額列 amt があるので、修飾名は chap1 になります。修飾名は、集計関数 (SUM、AVG、MAX、MIN、COUNT、STDEV、または ANY) のいずれかの引数として使用できます。</span><span class="sxs-lookup"><span data-stu-id="b622d-106">For example, if the parent chapter, chap1, contains a child chapter, chap2, that has an amount column, amt, then the qualified name would be chap1.chap2.amt. The qualified name may then be used as an argument to one of the aggregate functions (SUM, AVG, MAX, MIN, COUNT, STDEV, or ANY).</span></span>

