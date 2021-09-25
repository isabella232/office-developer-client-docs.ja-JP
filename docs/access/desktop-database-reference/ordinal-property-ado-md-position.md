---
title: Ordinal プロパティ (ADO MD Position)
TOCTitle: Ordinal property (ADO MD Position)
ms:assetid: fb132ab5-d2b5-317d-e885-5e37ddaf90fb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250284(v=office.15)
ms:contentKeyID: 48548861
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c82565fec9dea3b985185dfc198861caca9cbe6f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593916"
---
# <a name="ordinal-property-ado-md-position"></a>Ordinal プロパティ (ADO MD Position)


**適用先**: Access 2013、Office 2013

軸に沿った位置を一意に識別します。

## <a name="return-values"></a>戻り値

長整数型 (**Long**) の値を取得します。値の取得のみが可能です。

## <a name="remarks"></a>注釈

[Position](position-object-ado-md.md) オブジェクトの **Ordinal** プロパティは、[Positions](positions-collection-ado-md.md) コレクション内の **Position** のインデックスに対応します。

**Cellset** オブジェクトの **Item** プロパティでそれぞれの軸に沿って [Position](item-property-ado-md-cellset.md) オブジェクトの [Ordinal](cellset-object-ado-md.md) プロパティを使用することで、セルをすばやく取得できます。

