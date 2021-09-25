---
title: AbsolutePosition プロパティ (ADO)
TOCTitle: AbsolutePosition property (ADO)
ms:assetid: 500be001-9fa1-177b-f19d-acf003a0cdc2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249259(v=office.15)
ms:contentKeyID: 48544787
ms.date: 10/17/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 10c88c26e80cf7a9102d2101e9cc048d45843164
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586349"
---
# <a name="absoluteposition-property-ado"></a>AbsolutePosition プロパティ (ADO)

**適用先**: Access 2013、Office 2013

[Recordset](recordset-object-ado.md) オブジェクト内のカレント レコードの位置を表す値を示します。

## <a name="settings-and-return-values"></a>設定および戻り値

1 から **Recordset** オブジェクトのレコード数 ([RecordCount](recordcount-property-ado.md)) までの長整数型 (**Long**) の値を設定するか、または [PositionEnum](positionenum.md) 値の 1 つを取得します。

## <a name="remarks"></a>注釈

**AbsolutePosition プロパティを設定** するには、使用している OLE DB プロバイダーが IRowsetLocate インターフェイスを実装する必要があります。

Accessing the **AbsolutePosition** property of a **Recordset** that was opened with either a forward-only or dynamic cursor raises the error **adErrFeatureNotAvailable**. With other cursor types, the correct position will be returned as long as the provider supports the IRowsetScroll interface. プロバイダーが *IRowsetScroll* インターフェイスをサポートしていない場合、プロパティは **adPosUnknown に設定されます**。 プロバイダーが *IRowsetScroll* をサポートするかどうかを判断するには、プロバイダーのドキュメントを参照してください。

**AbsolutePosition** プロパティを使用すると、 **Recordset** オブジェクトでのレコードの順序位置に基づいて特定のレコードに移動したり、カレント レコードの順序位置を調べたりできます。このプロパティを使用するには、プロバイダーが必要な機能をサポートしている必要があります。

[AbsolutePosition](absolutepage-property-ado.md) は、 **AbsolutePage** プロパティと同じく 1 から始まる値で、 **Recordset** の先頭レコードがカレント レコードの場合に 1 になります。 **Recordset** オブジェクトのレコード総数は、 [RecordCount](recordcount-property-ado.md) プロパティから取得できます。

**AbsolutePosition** プロパティを設定すると、現在のキャッシュ内のレコードに対しても、ADO は指定したレコードから始まる新しいレコード グループでキャッシュを再読み込みします。 [CacheSize](cachesize-property-ado.md) プロパティにより、このグループのサイズが決定されます。


> [!NOTE]
> [!メモ] 代替レコード番号として **AbsolutePosition** プロパティを使用することはできません。 レコードの位置は、それより前のレコードが削除されると変わります。 また、 **Recordset** オブジェクトを照会し直したり、開き直したりした場合、同じレコードの **AbsolutePosition** が以前と同じになる保証はありません。 ブックマークは、特定の位置に保持して戻す推奨される方法であり、すべての種類の Recordset オブジェクトを配置する唯一 **の方法** です。


