---
title: Axis オブジェクト (ADO MD)
TOCTitle: Axis object (ADO MD)
ms:assetid: a4332b69-8900-08f1-a4e2-9395d005ed42
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249763(v=office.15)
ms:contentKeyID: 48546807
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 23fdb0d9ba636ae58fa19b42d5a8a47cb01d4ab2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720731"
---
# <a name="axis-object-ado-md"></a>Axis オブジェクト (ADO MD)


**適用されます**Access 2013、Office 2013。

1 つ以上の次元の選択されたメンバーを含む、セルセットの位置またはフィルターの軸を表します。

## <a name="remarks"></a>解説

**Axis** オブジェクトは、 [Axes](axes-collection-ado-md.md) コレクションに含めるか、または [Cellset](filteraxis-property-ado-md.md) の [FilterAxis](cellset-object-ado-md.md) プロパティによって返すことができます。

**Axis** オブジェクトのコレクションおよびプロパティを使用すると、次の操作を実行できます。

- **Name** プロパティを使用して、 [Axis](name-property-ado-md.md) を識別します。

- **Positions** コレクションを使用して、 [Axis](positions-collection-ado-md.md) に沿った位置に反復処理を実行します。

- **DimensionCount** プロパティを使用して、 [Axis](dimensioncount-property-ado-md.md) 上の次元の数を取得します。

- 標準の ADO **Properties** コレクションを使用して、 [Axis](properties-collection-ado.md) のプロバイダー固有の属性を取得します。

