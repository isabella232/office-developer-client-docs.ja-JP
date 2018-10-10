---
title: フィルター適用済みの階層 Recordset を保存する
TOCTitle: Persisting Filtered and Hierarchical Recordsets
ms:assetid: 3648a997-dac7-d8a3-3cca-a6827f26a4f0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249120(v=office.15)
ms:contentKeyID: 48544162
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d29fe867933bdff93d064a95a4fc95c65e8605f8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477342"
---
# <a name="persisting-filtered-and-hierarchical-recordsets"></a>フィルター適用済みの階層 Recordset を保存する


**適用されます**Access 2013 |。Office 2013

[Recordset](filter-property-ado.md) で **Filter** プロパティが有効になっている場合、フィルターでアクセスできる行のみが保存されます。 **Recordset** が階層の場合、現在の子 **Recordset** とその子が、親 **Recordset** と共に保存されます。子 **Recordset** の **Save** メソッドを呼び出すと、子とそのすべての子は保存されますが、親は保存されません。階層 **Recordset** の詳細については、「 [9 章: データ シェイプ](chapter-9-data-shaping.md)」を参照してください。


> [!NOTE]
> <P>[!メモ] 階層 <STRONG>Recordset</STRONG> (データ シェイプ) を XML 形式で保存する場合、いくつかの制限が適用されます。詳細については、「 <A href="hierarchical-recordsets-in-xml.md">XML の階層 Recordset</A>」を参照してください。</P>


