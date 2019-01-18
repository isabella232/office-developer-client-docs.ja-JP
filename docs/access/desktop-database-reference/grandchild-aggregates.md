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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722159"
---
# <a name="grandchild-aggregates"></a>孫の集計


**適用されます**Access 2013、Office 2013。

Shape コマンド句に作成されるチャプター列には、(通常は AS キーワードを使って*チャプター エイリアス名*を指定ことがあります。 列が含まれている子を識別する完全修飾名を持つシェイプされた**Recordset**のどのチャプター内の任意の列を識別することがあります。 など chap1、親章には、子の章では、chap2 が含まれている場合、amt、チャプター列を持つし、修飾名は chap1.chap2.amt になります。集計関数 (SUM、AVG、MAX、MIN、カウント、標準偏差、またはいずれか) のいずれかの引数として、修飾名を使用し、可能性があります。

