---
title: Axis オブジェクト (ADO MD)
TOCTitle: Axis object (ADO MD)
ms:assetid: a4332b69-8900-08f1-a4e2-9395d005ed42
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249763(v=office.15)
ms:contentKeyID: 48546807
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 057fa3c22c399f6f573a3ee2028cd7a80d8ad937
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602921"
---
# <a name="axis-object-ado-md"></a>Axis オブジェクト (ADO MD)


**適用先**: Access 2013、Office 2013

1 つ以上の次元の選択されたメンバーを含む、セルセットの位置またはフィルターの軸を表します。

## <a name="remarks"></a>注釈

**Axis** オブジェクトは、[Axes](axes-collection-ado-md.md) コレクションに含めるか、または [Cellset](cellset-object-ado-md.md) の [FilterAxis](filteraxis-property-ado-md.md) プロパティによって返すことができます。

**Axis** オブジェクトのコレクションおよびプロパティを使用すると、次の操作を実行できます。

- **Name** プロパティを使用して、 [Axis](name-property-ado-md.md) を識別します。

- **Positions** コレクションを使用して、 [Axis](positions-collection-ado-md.md) に沿った位置に反復処理を実行します。

- **DimensionCount** プロパティを使用して、 [Axis](dimensioncount-property-ado-md.md) 上の次元の数を取得します。

- 標準の ADO **Properties** コレクションを使用して、 [Axis](properties-collection-ado.md) のプロバイダー固有の属性を取得します。

