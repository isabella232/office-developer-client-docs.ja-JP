---
title: AbsolutePosition プロパティ (ADO)
TOCTitle: AbsolutePosition property (ADO)
ms:assetid: 500be001-9fa1-177b-f19d-acf003a0cdc2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249259(v=office.15)
ms:contentKeyID: 48544787
ms.date: 10/17/2018
mtps_version: v=office.15
ms.openlocfilehash: a090630b5db741f761314f598fcc783dd124d1cf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881861"
---
# <a name="absoluteposition-property-ado"></a>AbsolutePosition プロパティ (ADO)

**適用されます**Access 2013、Office 2013。

[Recordset](recordset-object-ado.md) オブジェクト内のカレント レコードの位置を表す値を示します。

## <a name="settings-and-return-values"></a>設定値および戻り値

1 から **Recordset** オブジェクトのレコード数 ([RecordCount](recordcount-property-ado.md)) までの長整数型 (**Long**) の値を設定するか、または [PositionEnum](positionenum.md) 値の 1 つを取得します。

## <a name="remarks"></a>備考

**AbsolutePosition**プロパティを設定するには、ADO は、使用している OLE DB プロバイダーがクラス インターフェイスを実装する必要があります。

**AbsolutePosition**をアクセスするか、前方のみまたは動的カーソルで開かれた**レコード セット**のプロパティは、エラー **adErrFeatureNotAvailable**を発生します。 他のカーソル型では、プロバイダーが IRowsetScroll インターフェイスをサポートしている限り、正しい位置が返されます。 プロバイダーが*IRowsetScroll*インターフェイスをサポートしていない場合、プロパティは**adPosUnknown**に設定します。 *IRowsetScroll*をサポートしているかどうかは、プロバイダーのマニュアルを参照してください。

**AbsolutePosition** プロパティを使用すると、 **Recordset** オブジェクトでのレコードの順序位置に基づいて特定のレコードに移動したり、カレント レコードの順序位置を調べたりできます。このプロパティを使用するには、プロバイダーが必要な機能をサポートしている必要があります。

[AbsolutePosition](absolutepage-property-ado.md) は、 **AbsolutePage** プロパティと同じく 1 から始まる値で、 **Recordset** の先頭レコードがカレント レコードの場合に 1 になります。 **Recordset** オブジェクトのレコード総数は、 [RecordCount](recordcount-property-ado.md) プロパティから取得できます。

**AbsolutePosition**プロパティを設定すると、現在のキャッシュ内のレコードになっている場合でも、ADO のレコードの指定したレコードで始まる新しいグループがキャッシュに再読み込みします。 読み込まれるレコード数は、 [CacheSize](cachesize-property-ado.md) プロパティにより決まります。


> [!NOTE]
> [!メモ] **AbsolutePosition** プロパティをレコード番号の代わりに使用しないでください。 レコードの位置は、それより前のレコードが削除されると変わります。 また、 **Recordset** オブジェクトを照会し直したり、開き直したりした場合、同じレコードの **AbsolutePosition** が以前と同じになる保証はありません。 ブックマークはいるデータを保持し、指定の位置に戻るための推奨手段であり、すべてのタイプの**Recordset**オブジェクトで位置を決定する唯一の方法です。


