---
title: 孫の集計
TOCTitle: Grandchild Aggregates
ms:assetid: ea5e2e1f-f3d5-f851-623a-a5d1385fe206
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250188(v=office.15)
ms:contentKeyID: 48548462
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e79cfe863e80e70e75d7f8e65c10764df67a39df
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478759"
---
# <a name="grandchild-aggregates"></a><span data-ttu-id="d1db8-102">孫の集計</span><span class="sxs-lookup"><span data-stu-id="d1db8-102">Grandchild Aggregates</span></span>


<span data-ttu-id="d1db8-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="d1db8-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d1db8-104">Shape コマンド句に作成されるチャプター列には、(通常は AS キーワードを使って*チャプター エイリアス名*を指定ことがあります。</span><span class="sxs-lookup"><span data-stu-id="d1db8-104">The chapter column created in a clause of a shape command may be given a *chapter-alias name* (typically with the AS keyword).</span></span> <span data-ttu-id="d1db8-105">列が含まれている子を識別する完全修飾名を持つシェイプされた**Recordset**のどのチャプター内の任意の列を識別することがあります。</span><span class="sxs-lookup"><span data-stu-id="d1db8-105">You may identify any column in any chapter of the shaped **Recordset** with a fully qualified name identifying the child containing the column.</span></span> <span data-ttu-id="d1db8-106">など chap1、親章には、子の章では、chap2 が含まれている場合、amt、チャプター列を持つし、修飾名は chap1.chap2.amt になります。集計関数 (SUM、AVG、MAX、MIN、カウント、標準偏差、またはいずれか) のいずれかの引数として、修飾名を使用し、可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d1db8-106">For example, if the parent chapter, chap1, contains a child chapter, chap2, that has an amount column, amt, then the qualified name would be chap1.chap2.amt. The qualified name may then be used as an argument to one of the aggregate functions (SUM, AVG, MAX, MIN, COUNT, STDEV, or ANY).</span></span>

