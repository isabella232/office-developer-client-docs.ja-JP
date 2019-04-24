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
# <a name="grandchild-aggregates"></a>孫の集計


**適用先:** Access 2013、Office 2013

shape コマンドの句で作成されたチャプター列には、(通常は as キーワードを使用して)*チャプターエイリアス名*を指定できます。 シェイプされた**Recordset**の任意のチャプター内の列は、その列が含まれている子を識別する完全修飾名で識別できます。 たとえば、親チャプター chap1 が含まれている場合は、chap2 という子チャプターが含まれているとします。これには、金額列 amt があるので、修飾名は chap1 になります。修飾名は、集計関数 (SUM、AVG、MAX、MIN、COUNT、STDEV、または ANY) のいずれかの引数として使用できます。

