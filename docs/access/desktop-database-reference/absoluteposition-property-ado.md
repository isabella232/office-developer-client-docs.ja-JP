---
title: AbsolutePosition プロパティ (ADO)
TOCTitle: AbsolutePosition Property (ADO)
ms:assetid: 500be001-9fa1-177b-f19d-acf003a0cdc2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249259(v=office.15)
ms:contentKeyID: 48544787
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3258ffcab87b16e4931c9881a8e8d1cd2143262f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479148"
---
# <a name="absoluteposition-property-ado"></a>AbsolutePosition プロパティ (ADO)


**適用されます**Access 2013 |。Office 2013

[Recordset](recordset-object-ado.md) オブジェクト内のカレント レコードの位置を表す値を示します。

## <a name="settings-and-return-values"></a>設定値と戻り値

1 から **Recordset** オブジェクトのレコード数 ([RecordCount](recordcount-property-ado.md)) までの長整数型 (**Long**) の値を設定するか、または [PositionEnum](positionenum.md) 値の 1 つを取得します。

## <a name="remarks"></a>解説

ADO の **AbsolutePosition** プロパティを設定するには、使用する OLE DB プロバイダーが IRowsetLocate インターフェイスを実装している必要があります。

**AbsolutePosition**をアクセスするか、前方のみまたは動的カーソルで開かれた**レコード セット**のプロパティは、エラー **adErrFeatureNotAvailable**を発生します。 他のカーソル型では、プロバイダーが IRowsetScroll インターフェイスをサポートしている限り、正しい位置が返されます。 プロバイダーが*IRowsetScroll*インターフェイスをサポートしていない場合、プロパティは**adPosUnknown**に設定します。 *IRowsetScroll*をサポートしているかどうかは、プロバイダーのマニュアルを参照してください。

**AbsolutePosition** プロパティを使用すると、 **Recordset** オブジェクトでのレコードの順序位置に基づいて特定のレコードに移動したり、カレント レコードの順序位置を調べたりできます。このプロパティを使用するには、プロバイダーが必要な機能をサポートしている必要があります。

[AbsolutePosition](absolutepage-property-ado.md) は、 **AbsolutePage** プロパティと同じく 1 から始まる値で、 **Recordset** の先頭レコードがカレント レコードの場合に 1 になります。 **Recordset** オブジェクトのレコード総数は、 [RecordCount](recordcount-property-ado.md) プロパティから取得できます。

**AbsolutePosition** プロパティを設定すると、たとえ現在のキャッシュ内のレコードに設定した場合でも、ADO は指定されたレコードから始まる新しいレコード群をキャッシュに再読み込みします。読み込まれるレコード数は、 [CacheSize](cachesize-property-ado.md) プロパティにより決まります。


> [!NOTE]
> <P>[!メモ] <STRONG>AbsolutePosition</STRONG> プロパティをレコード番号の代わりに使用しないでください。レコードの位置は、それより前のレコードが削除されると変わります。また、 <STRONG>Recordset</STRONG> オブジェクトを照会し直したり、開き直したりした場合、同じレコードの <STRONG>AbsolutePosition</STRONG> が以前と同じになる保証はありません。ブックマークが、特定の位置を保持してその位置に戻るための推奨手段であり、すべての種類の <STRONG>Recordset</STRONG> オブジェクトで位置を指定するための唯一の手段です。</P>


