---
title: UnderlyingValue プロパティ (ADO)
TOCTitle: UnderlyingValue property (ADO)
ms:assetid: f84f4c1c-2bd4-a725-3575-ed063ead13c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250262(v=office.15)
ms:contentKeyID: 48548782
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6d1618a0cb310c1e564fe18289da6a2d35e91d0b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717294"
---
# <a name="underlyingvalue-property-ado"></a>UnderlyingValue プロパティ (ADO)


**適用されます**Access 2013、Office 2013。



データベース内の [Field](field-object-ado.md) オブジェクトの現在の値を示します。

## <a name="return-value"></a>戻り値

**Field** の値を示すバリアント型 ( **Variant** ) の値を返します。

## <a name="remarks"></a>解説

データベースから現在のフィールド値を返すには、 **UnderlyingValue** プロパティを使用します。 **UnderlyingValue** プロパティ内のフィールド値は、トランザクションで参照できる値であり、別のトランザクションによる最近の更新の結果である可能性があります。この値は、 [Recordset](originalvalue-property-ado.md) に最初に返された値を反映する [OriginalValue](recordset-object-ado.md) プロパティとは異なる場合があります。

これは [Resync](resync-method-ado.md) メソッドを使用した場合と似ていますが、 **UnderlyingValue** プロパティは現在のレコードから特定のフィールドの値のみを返します。この値は、 [Resync](resync-method-ado.md) メソッドが [Value](value-property-ado.md) プロパティを置き換えるために使用する値と同じです。

このプロパティを **OriginalValue** プロパティと共に使用すると、一括更新で発生する競合を解消できます。

## <a name="record"></a>Record

[Record](record-object-ado.md) オブジェクトの場合、 [Update](update-method-ado.md) が呼び出される前に追加されたフィールドについては、このプロパティは空になります。

