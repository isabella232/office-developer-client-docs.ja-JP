---
title: 孫の集計
TOCTitle: Grandchild aggregates
ms:assetid: ea5e2e1f-f3d5-f851-623a-a5d1385fe206
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250188(v=office.15)
ms:contentKeyID: 48548462
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d55a304c05076a83af25265d51cb0837a7ea1459
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568958"
---
# <a name="grandchild-aggregates"></a>孫の集計


**適用先:** Access 2013、Office 2013

shape コマンドの句で作成されたチャプター列には、チャプター エイリアス名 *(通常* は AS キーワード付き) を指定できます。 列を含む子を識別する完全修飾名を持つ、図形 **の Recordset** の任意のチャプター内の任意の列を識別できます。 たとえば、親チャプター chap1 に、金額列 amt を持つ子チャプター chap2 が含まれている場合、修飾名は chap1.chap2.amt となります。次に、修飾名を集計関数 (SUM、AVG、MAX、MIN、COUNT、STDEV、ANY) の 1 つの引数として使用できます。

