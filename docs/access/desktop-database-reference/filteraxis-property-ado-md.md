---
title: filteraxis プロパティ (ADO MD)
TOCTitle: FilterAxis property (ADO MD)
ms:assetid: 36720d77-4b16-1d17-6d80-d35265f4a8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249124(v=office.15)
ms:contentKeyID: 48544172
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3b1f9c2bcc4ed4f3314a697d4a0eae8415bc4f62
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292455"
---
# <a name="filteraxis-property-ado-md"></a>filteraxis プロパティ (ADO MD)


**適用先:** Access 2013、Office 2013

現在のセルセットのフィルター情報を示します。

## <a name="return-values"></a>戻り値

[Axis](axis-object-ado-md.md) オブジェクトを取得します。値の取得のみが可能です。

## <a name="remarks"></a>注釈

**FilterAxis** プロパティを使用すると、データをスライスするために使用した次元の情報を取得できます。 [Axis](dimensioncount-property-ado-md.md) オブジェクトの **DimensionCount** プロパティは、スライスする次元の数を返します。この軸には通常、行が 1 つだけ含まれます。

**FilterAxis** によって取得される [Axis](filteraxis-property-ado-md.md) オブジェクトは、 [Cellset](axes-collection-ado-md.md) オブジェクトの [Axes](cellset-object-ado-md.md) コレクションには含まれません。

