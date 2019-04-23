---
title: AbsolutePosition プロパティ (ADO)
TOCTitle: AbsolutePosition property (ADO)
ms:assetid: 500be001-9fa1-177b-f19d-acf003a0cdc2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249259(v=office.15)
ms:contentKeyID: 48544787
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9b5e25e014c6e93d35e3621bb9b5b3c21d5e77f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281978"
---
# <a name="absoluteposition-property-ado"></a>AbsolutePosition プロパティ (ADO)

**適用先:** Access 2013、Office 2013

[Recordset](recordset-object-ado.md) オブジェクト内のカレント レコードの位置を表す値を示します。

## <a name="settings-and-return-values"></a>設定値と戻り値

1 から **Recordset** オブジェクトのレコード数 ([RecordCount](recordcount-property-ado.md)) までの長整数型 (**Long**) の値を設定するか、または [PositionEnum](positionenum.md) 値の 1 つを取得します。

## <a name="remarks"></a>注釈

ADO で**AbsolutePosition**プロパティを設定するには、使用する OLE DB プロバイダーが IRowsetLocate インターフェイスを実装している必要があります。

Accessing the **AbsolutePosition** property of a **Recordset** that was opened with either a forward-only or dynamic cursor raises the error **adErrFeatureNotAvailable**. With other cursor types, the correct position will be returned as long as the provider supports the IRowsetScroll interface. プロバイダーが*IRowsetScroll*インターフェイスをサポートしていない場合、このプロパティは**adposunknown**に設定されます。 *IRowsetScroll*をサポートしているかどうかについては、プロバイダーのドキュメントを参照してください。

**AbsolutePosition** プロパティを使用すると、 **Recordset** オブジェクトでのレコードの順序位置に基づいて特定のレコードに移動したり、カレント レコードの順序位置を調べたりできます。このプロパティを使用するには、プロバイダーが必要な機能をサポートしている必要があります。

[AbsolutePosition](absolutepage-property-ado.md) は、 **AbsolutePage** プロパティと同じく 1 から始まる値で、 **Recordset** の先頭レコードがカレント レコードの場合に 1 になります。 **Recordset** オブジェクトのレコード総数は、 [RecordCount](recordcount-property-ado.md) プロパティから取得できます。

**AbsolutePosition**プロパティを設定すると、現在のキャッシュ内のレコードに設定されている場合でも、ADO は指定されたレコードから始まる新しいレコードグループをキャッシュに再読み込みします。 [CacheSize](cachesize-property-ado.md) プロパティにより、このグループのサイズが決定されます。


> [!NOTE]
> [!メモ] 代替レコード番号として **AbsolutePosition** プロパティを使用することはできません。 レコードの位置は、それより前のレコードが削除されると変わります。 また、 **Recordset** オブジェクトを照会し直したり、開き直したりした場合、同じレコードの **AbsolutePosition** が以前と同じになる保証はありません。 ブックマークは、特定の位置を保持してその位置に戻るための推奨手段であり、すべての種類の**Recordset**オブジェクトで位置を指定するための唯一の方法です。


