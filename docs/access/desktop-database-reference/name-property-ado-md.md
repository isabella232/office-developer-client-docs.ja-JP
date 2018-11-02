---
title: Name プロパティ (ADO MD)
TOCTitle: Name property (ADO MD)
ms:assetid: 31ea6dad-c464-3af7-4b7a-086900656c2c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249093(v=office.15)
ms:contentKeyID: 48544065
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 971a528c0efe97626f08ff94490e8aee25230f60
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926536"
---
# <a name="name-property-ado-md"></a>Name プロパティ (ADO MD)


**適用されます**Access 2013、Office 2013。

オブジェクトの名前を示します。

## <a name="return-values"></a>戻り値

文字列型 ( **String** ) の値を取得します。値の取得のみが可能です。

## <a name="remarks"></a>解説

オブジェクトの **Name** プロパティを序数参照で取得できます。その後は、名前を使用して直接オブジェクトを参照できます。たとえば、cdf.CubeDefs(0).Name によって "Bobs Video Store" を取得すると、この [CubeDef](cubedef-object-ado-md.md) を cdf.CubeDefs("Bobs Video Store") として参照できるようになります。

