---
title: フィルター済みのレコードセットと階層レコードセットの永続化
TOCTitle: Persisting filtered and hierarchical Recordsets
ms:assetid: 3648a997-dac7-d8a3-3cca-a6827f26a4f0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249120(v=office.15)
ms:contentKeyID: 48544162
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1332d4348c993f94d8b2ee61280b8b35c02324c4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287588"
---
# <a name="persisting-filtered-and-hierarchical-recordsets"></a>フィルター済みのレコードセットと階層レコードセットの永続化


**適用先:** Access 2013、Office 2013

[Recordset](filter-property-ado.md) で **Filter** プロパティが有効になっている場合、フィルターでアクセスできる行のみが保存されます。 **Recordset** が階層の場合、現在の子 **Recordset** とその子が、親 **Recordset** と共に保存されます。子 **Recordset** の **Save** メソッドを呼び出すと、子とそのすべての子は保存されますが、親は保存されません。階層 **Recordset** の詳細については、「 [9 章: データ シェイプ](chapter-9-data-shaping.md)」を参照してください。


> [!NOTE]
> [!メモ] 階層 **Recordset** (データ シェイプ) を XML 形式で保存する場合、いくつかの制限が適用されます。詳細については、「 [XML の階層 Recordset](hierarchical-recordsets-in-xml.md)」を参照してください。


