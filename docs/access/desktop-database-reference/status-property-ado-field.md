---
title: Status プロパティ (ADO Field)
TOCTitle: Status property (ADO Field)
ms:assetid: 7a7b45e8-2934-2e8e-77fa-a4f38272548d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249507(v=office.15)
ms:contentKeyID: 48545795
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 877a7d17b0f5ad9d5b0c16e6ff2497083c5276a9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568384"
---
# <a name="status-property-ado-field"></a>Status プロパティ (ADO Field)


**適用先:** Access 2013、Office 2013

[Field](field-object-ado.md) オブジェクトのステータスを示します。

## <a name="return-value"></a>戻り値

[FieldStatusEnum](fieldstatusenum.md) 値を返します。既定値は **adFieldOK** です。

## <a name="remarks"></a>注釈

[Recordset](recordset-object-ado.md) オブジェクトのフィールドについては、このプロパティは常に **adFieldOK** を返します。

[Record](fields-collection-ado.md) オブジェクトの [Fields](record-object-ado.md) コレクションに対する追加や削除は、 [Update](update-method-ado.md) メソッドが呼び出されるまでキャッシュされます。 **Status** プロパティを使用すると、正常に追加または削除されたフィールドを特定できます。

パフォーマンスを向上させるため、スキーマの変更は **Update** が呼び出されるまでキャッシュされ、その変更は共有的バッチ更新で反映されます。 **Update** メソッドが呼び出されなかった場合、サーバーは更新されません。 更新に失敗した場合は、エラーが返され、 **Status** プロパティは操作とエラー ステータス コードを組み合わせた値になります。 たとえば、 **adFieldPendingInsert** **OR** **adFieldPermissionDenied** です。 各 **Field** の **Status** プロパティを使用すると、 **Field** が追加、変更、または削除されなかった理由を調べることができます。 **状態** は、Record でのみ意味のある公開 **です**。**Recordset** ではなく Fields **コレクション** です。**Fields** コレクション。

**Field** を追加、変更、または削除するときに 2 つの問題が発生する可能性があります。ユーザーが **Field** を削除すると、 **Fields** コレクションから削除されたことを示すマークが付けられます。ユーザーが権限を与えられていない **Field** を削除しようとしたために、それ以降の **Update** がエラーを返す場合、 **Field** のステータスは **adFieldPermissionDenied** **OR** **adFieldPendingDelete** になります。 [CancelUpdate](cancelupdate-method-ado.md) メソッドを呼び出すと、元の値が復元され、 **Status** は **adFieldOK** になります。同様に、新規 **Field** が追加され、不適切な値が割り当てられたために、 **Update** メソッドがエラーを返す場合があります。この場合、新規 **Field** は **Fields** コレクションに追加されますが、ステータスは **adFieldPendingInsert** および場合によっては **adFieldCantCreate** になります。新規 **Field** に適切な値を指定し、 **Update** を再度呼び出すことができます。代わりに **Resync** を呼び出すと、プロバイダーに再度クエリが実行されます。

