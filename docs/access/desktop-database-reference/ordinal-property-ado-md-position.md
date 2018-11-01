---
title: Ordinal プロパティ (ADO MD Position)
TOCTitle: Ordinal Property (ADO MD Position)
ms:assetid: fb132ab5-d2b5-317d-e885-5e37ddaf90fb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250284(v=office.15)
ms:contentKeyID: 48548861
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: efe0fcd48d3575651096b30853c3680b0284cf52
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876800"
---
# <a name="ordinal-property-ado-md-position"></a>Ordinal プロパティ (ADO MD Position)


**適用されます**Access 2013、Office 2013。

軸に沿った位置を一意に識別します。

## <a name="return-values"></a>戻り値

長整数型 ( **Long** ) の値を取得します。値の取得のみが可能です。

## <a name="remarks"></a>解説

**Position** オブジェクトの [Ordinal](position-object-ado-md.md) プロパティは、 **Positions** コレクション内の [Position](positions-collection-ado-md.md) のインデックスに対応します。

**Cellset** オブジェクトの **Item** プロパティでそれぞれの軸に沿って [Position](item-property-ado-md-cellset.md) オブジェクトの [Ordinal](cellset-object-ado-md.md) プロパティを使用することで、セルをすばやく取得できます。

