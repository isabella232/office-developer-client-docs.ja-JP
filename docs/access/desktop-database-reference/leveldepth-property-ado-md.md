---
title: leveldepth プロパティ (ADO MD)
TOCTitle: LevelDepth property (ADO MD)
ms:assetid: ba680f1e-2731-ad6b-4cee-cd3d8d114788
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249894(v=office.15)
ms:contentKeyID: 48547366
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 664a21f8b642c8db27580993089268e5d7b6f4ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290007"
---
# <a name="leveldepth-property-ado-md"></a>leveldepth プロパティ (ADO MD)


**適用先:** Access 2013、Office 2013

階層のルートとメンバーとの間にあるレベルの数を示します。

## <a name="return-values"></a>戻り値

長整数型 (**Long**) の値を取得します。値の取得のみが可能です。

## <a name="remarks"></a>注釈

**LevelDepth** プロパティを使用して、階層のルート レベルから [Member](member-object-ado-md.md) オブジェクトまでの距離を調べます。ルート レベルにあるメンバーの **LevelDepth** は 0 です。このプロパティは、[Level](level-object-ado-md.md) オブジェクトの [Depth](depth-property-ado-md.md) プロパティに対応します。

