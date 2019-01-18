---
title: Ordinal プロパティ (ADO MD Cell)
TOCTitle: Ordinal property (ADO MD Cell)
ms:assetid: be705823-6c5e-0c8f-f780-87df19423a72
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249924(v=office.15)
ms:contentKeyID: 48547462
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 91b8d66929e360f88385b6773a03fcaffb79161d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717413"
---
# <a name="ordinal-property-ado-md-cell"></a>Ordinal プロパティ (ADO MD Cell)


**適用されます**Access 2013、Office 2013。

セルセット内の位置によってセルを一意に識別します。

## <a name="return-values"></a>戻り値

長整数型 ( **Long** ) の値を取得します。値の取得のみが可能です。

## <a name="remarks"></a>解説

セルの序数値はセルセット内のセルを一意に識別します。概念的は、セルセット内のセルはセルセットが *p* 番号が付けられます。ここで、*p* は[軸](axes-collection-ado-md.md)の数です。セルは行優先でアドレス指定されます。

セルの序数値は [Cellset](item-property-ado-md-cellset.md) オブジェクトの [Item](cellset-object-ado-md.md) プロパティと共に使用して、 [Cell](cell-object-ado-md.md) を迅速に取得できます。

