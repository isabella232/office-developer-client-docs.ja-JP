---
title: Number プロパティ (ADO)
TOCTitle: Number Property (ADO)
ms:assetid: b5103af5-356b-ec74-cd62-86e59467d491
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249868(v=office.15)
ms:contentKeyID: 48547243
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4e9b048643b1892197f610ef6d53e6ba46b170d8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476204"
---
# <a name="number-property-ado"></a>Number プロパティ (ADO)


**適用されます**Access 2013 |。Office 2013

[Error](error-object-ado.md) オブジェクトを一意に識別する数値を示します。

## <a name="return-value"></a>戻り値

**ErrorValueEnum** 定数のいずれかに対応する長整数型 ( [Long](errorvalueenum.md) ) の値を返します。

## <a name="remarks"></a>解説

**Number** プロパティは、発生したエラーを調べるために使用します。プロパティの値は、エラー条件に対応した一意な数値です。

[Errors](errors-collection-ado.md)コレクションは、いずれかの 16 進形式 (例: 0x80004005) または長整数型 (例: 2147467259) で HRESULT を返します。 これらの Hresult は、OLE DB または偶数の OLE 自体など、基になるコンポーネントで発生する可能性がします。 これらの数値の詳細については、の第 16 章を参照してください、 *OLE DB プログラマ リファレンスです*。

