---
title: LevelDepth プロパティ (ADO MD)
TOCTitle: LevelDepth property (ADO MD)
ms:assetid: ba680f1e-2731-ad6b-4cee-cd3d8d114788
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249894(v=office.15)
ms:contentKeyID: 48547366
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8ea31e6197e1c646632a312ed417bbbd1be9f4d7
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923505"
---
# <a name="leveldepth-property-ado-md"></a>LevelDepth プロパティ (ADO MD)


**適用されます**Access 2013、Office 2013。

階層のルートとメンバーとの間にあるレベルの数を示します。

## <a name="return-values"></a>戻り値

長整数型 ( **Long** ) の値を取得します。値の取得のみが可能です。

## <a name="remarks"></a>解説

**LevelDepth** プロパティを使用して、階層のルート レベルから [Member](member-object-ado-md.md) オブジェクトまでの距離を調べます。ルート レベルにあるメンバーの **LevelDepth** は 0 です。このプロパティは、 [Level](depth-property-ado-md.md) オブジェクトの [Depth](level-object-ado-md.md) プロパティに対応します。

