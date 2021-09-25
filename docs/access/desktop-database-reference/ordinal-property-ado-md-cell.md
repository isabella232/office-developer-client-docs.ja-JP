---
title: Ordinal プロパティ (ADO MD Cell)
TOCTitle: Ordinal property (ADO MD Cell)
ms:assetid: be705823-6c5e-0c8f-f780-87df19423a72
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249924(v=office.15)
ms:contentKeyID: 48547462
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ba897ff825725eb7ec43d695934bb4840dedee6b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597129"
---
# <a name="ordinal-property-ado-md-cell"></a>Ordinal プロパティ (ADO MD Cell)


**適用先**: Access 2013、Office 2013

セルセット内の位置によってセルを一意に識別します。

## <a name="return-values"></a>戻り値

長整数型 (**Long**) の値を取得します。値の取得のみが可能です。

## <a name="remarks"></a>注釈

セルの序数値はセルセット内のセルを一意に識別します。概念的は、セルセット内のセルはセルセットが *p* 番号が付けられます。ここで、*p* は [軸](axes-collection-ado-md.md)の数です。セルは行優先でアドレス指定されます。

セルの序数値は [Cellset](cellset-object-ado-md.md) オブジェクトの [Item](item-property-ado-md-cellset.md) プロパティと共に使用して、[Cell](cell-object-ado-md.md) を迅速に取得できます。

