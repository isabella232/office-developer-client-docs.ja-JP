---
title: DrilledDown プロパティ (ADO MD)
TOCTitle: DrilledDown property (ADO MD)
ms:assetid: 1dfe728f-8da2-1d2b-7361-8689a0b088b4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248972(v=office.15)
ms:contentKeyID: 48543610
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 2cd7f38bc3adee25c5a4fa7765b94a289fc5b7b7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59553068"
---
# <a name="drilleddown-property-ado-md"></a>DrilledDown プロパティ (ADO MD)


**適用先:** Access 2013、Office 2013

軸上でメンバーの直下に子がないかどうかを示します。

## <a name="return-values"></a>戻り値

ブール型 (**Boolean**) の値を取得します。値の取得のみが可能です。**DrilledDown** プロパティは、軸上の現在のメンバーに子メンバーがない場合、**True** を返します。軸上の現在のメンバーに 1 つ以上の子メンバーがある場合、**DrilledDown** プロパティは **False** を返します。

## <a name="remarks"></a>注釈

**DrilledDown** プロパティを使用すると、軸上の現在のメンバーの直下に少なくとも 1 つの子があるかどうかを調べることができます。この情報は、メンバーを表示する際に役に立ちます。

このプロパティは、[Position](member-object-ado-md.md) オブジェクトに属している [Member](position-object-ado-md.md) オブジェクトのみでサポートされています。 **Level** オブジェクトに属する [Member](level-object-ado-md.md) オブジェクトからこのプロパティが参照されると、エラーが発生します。

