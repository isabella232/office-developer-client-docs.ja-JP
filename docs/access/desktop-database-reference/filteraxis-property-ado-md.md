---
title: FilterAxis プロパティ (ADO MD)
TOCTitle: FilterAxis Property (ADO MD)
ms:assetid: 36720d77-4b16-1d17-6d80-d35265f4a8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249124(v=office.15)
ms:contentKeyID: 48544172
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f298acf3a9250a0376ba31f5d3afc6b079ce0c78
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867707"
---
# <a name="filteraxis-property-ado-md"></a>FilterAxis プロパティ (ADO MD)


**適用されます**Access 2013、Office 2013。

現在のセルセットのフィルター情報を示します。

## <a name="return-values"></a>戻り値

[Axis](axis-object-ado-md.md) オブジェクトを取得します。値の取得のみが可能です。

## <a name="remarks"></a>解説

**FilterAxis** プロパティを使用すると、データをスライスするために使用した次元の情報を取得できます。 [Axis](dimensioncount-property-ado-md.md) オブジェクトの **DimensionCount** プロパティは、スライスする次元の数を返します。この軸には通常、行が 1 つだけ含まれます。

**FilterAxis** によって取得される [Axis](filteraxis-property-ado-md.md) オブジェクトは、 [Cellset](axes-collection-ado-md.md) オブジェクトの [Axes](cellset-object-ado-md.md) コレクションには含まれません。

