---
title: 孫の集計
TOCTitle: Grandchild aggregates
ms:assetid: ea5e2e1f-f3d5-f851-623a-a5d1385fe206
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250188(v=office.15)
ms:contentKeyID: 48548462
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bc7576eb8e1555ab8b00d2800242c7be24baca58
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947939"
---
# <a name="grandchild-aggregates"></a>孫の集計


**適用されます**Access 2013、Office 2013。

Shape コマンド句に作成されるチャプター列には、(通常は AS キーワードを使って*チャプター エイリアス名*を指定ことがあります。 列が含まれている子を識別する完全修飾名を持つシェイプされた**Recordset**のどのチャプター内の任意の列を識別することがあります。 など chap1、親章には、子の章では、chap2 が含まれている場合、amt、チャプター列を持つし、修飾名は chap1.chap2.amt になります。集計関数 (SUM、AVG、MAX、MIN、カウント、標準偏差、またはいずれか) のいずれかの引数として、修飾名を使用し、可能性があります。

