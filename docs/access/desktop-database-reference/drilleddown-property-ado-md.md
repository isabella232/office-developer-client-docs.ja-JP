---
title: DrilledDown プロパティ (ADO MD)
TOCTitle: DrilledDown property (ADO MD)
ms:assetid: 1dfe728f-8da2-1d2b-7361-8689a0b088b4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248972(v=office.15)
ms:contentKeyID: 48543610
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9d521176eeb2ac2e83ef05d05d3572dfba543812
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931002"
---
# <a name="drilleddown-property-ado-md"></a>DrilledDown プロパティ (ADO MD)


**適用されます**Access 2013、Office 2013。

軸上でメンバーの直下に子がないかどうかを示します。

## <a name="return-values"></a>戻り値

ブール型 ( **Boolean** ) の値を取得します。値の取得のみが可能です。 **DrilledDown** プロパティは、軸上の現在のメンバーに子メンバーがない場合、 **True** を返します。軸上の現在のメンバーに 1 つ以上の子メンバーがある場合、 **DrilledDown** プロパティは **False** を返します。

## <a name="remarks"></a>解説

**DrilledDown** プロパティを使用すると、軸上の現在のメンバーの直下に少なくとも 1 つの子があるかどうかを調べることができます。この情報は、メンバーを表示する際に役に立ちます。

このプロパティは、[Position](member-object-ado-md.md) オブジェクトに属している [Member](position-object-ado-md.md) オブジェクトのみでサポートされています。 **Level** オブジェクトに属する [Member](level-object-ado-md.md) オブジェクトからこのプロパティが参照されると、エラーが発生します。

