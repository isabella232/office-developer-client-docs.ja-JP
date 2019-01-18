---
title: FormattedValue プロパティ (ADO MD)
TOCTitle: FormattedValue property (ADO MD)
ms:assetid: ea7962f2-b08b-52c9-34e5-c5490c72662f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250189(v=office.15)
ms:contentKeyID: 48548464
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d750944cd42feb95b09f53382c54329ea0c32e1d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711596"
---
# <a name="formattedvalue-property-ado-md"></a>FormattedValue プロパティ (ADO MD)


**適用されます**Access 2013、Office 2013。

セル値の書式付き表示を示します。

## <a name="return-values"></a>戻り値

文字列型 ( **String** ) の値を取得します。値の取得のみが可能です。

## <a name="remarks"></a>解説

**FormattedValue** プロパティを使用すると、 [Cell](value-property-ado-md.md) オブジェクトの [Value](cell-object-ado-md.md) プロパティの書式付き表示の値を取得できます。たとえば、セルの値が 1056.87 で、この値がドルの額を表している場合、 **FormattedValue** プロパティは $1,056.87 になります。

