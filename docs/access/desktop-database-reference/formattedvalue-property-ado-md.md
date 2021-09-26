---
title: FormattedValue プロパティ (ADO MD)
TOCTitle: FormattedValue property (ADO MD)
ms:assetid: ea7962f2-b08b-52c9-34e5-c5490c72662f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250189(v=office.15)
ms:contentKeyID: 48548464
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 3be22eb3eb55a9c3a547e92b7b1ecf9de3a5f029
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626541"
---
# <a name="formattedvalue-property-ado-md"></a>FormattedValue プロパティ (ADO MD)


**適用先**: Access 2013、Office 2013

セル値の書式付き表示を示します。

## <a name="return-values"></a>戻り値

文字列型 (**String**) の値を取得します。値の取得のみが可能です。

## <a name="remarks"></a>注釈

**FormattedValue** プロパティを使用すると、[Cell](cell-object-ado-md.md) オブジェクトの [Value](value-property-ado-md.md) プロパティの書式付き表示の値を取得できます。たとえば、セルの値が 1056.87 で、この値がドルの額を表している場合、**FormattedValue** プロパティは $1,056.87 になります。

