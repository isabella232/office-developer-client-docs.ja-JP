---
title: Status プロパティ (ADO Field)
TOCTitle: Status Property (ADO Field)
ms:assetid: 7a7b45e8-2934-2e8e-77fa-a4f38272548d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249507(v=office.15)
ms:contentKeyID: 48545795
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 41534132fd4f199294e317310215d4f6e8ac5426
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603267"
---
# <a name="status-property-ado-field"></a>Status プロパティ (ADO Field)


**適用されます**Access 2013 |。Office 2013

[Field](field-object-ado.md) オブジェクトのステータスを示します。

<<<<<<< ヘッド
## <a name="return-value"></a>戻り値
=======
## <a name="return-value"></a>戻り値
>>>>>>> master

[FieldStatusEnum](fieldstatusenum.md) 値を返します。既定値は **adFieldOK** です。

## <a name="remarks"></a>解説

**Recordset** オブジェクトのフィールドについては、このプロパティは常に [adFieldOK](recordset-object-ado.md) を返します。

[Record](fields-collection-ado.md) オブジェクトの [Fields](record-object-ado.md) コレクションに対する追加や削除は、 [Update](update-method-ado.md) メソッドが呼び出されるまでキャッシュされます。 **Status** プロパティを使用すると、正常に追加または削除されたフィールドを特定できます。

パフォーマンスを向上させるため、スキーマの変更は **Update** が呼び出されるまでキャッシュされ、その変更は共有的バッチ更新で反映されます。 **Update** メソッドが呼び出されなかった場合、サーバーは更新されません。 更新に失敗した場合は、エラーが返され、 **Status** プロパティは操作とエラー ステータス コードを組み合わせた値になります。 たとえば、 **adFieldPendingInsert** **OR** **adFieldPermissionDenied** です。 各 **Field** の **Status** プロパティを使用すると、 **Field** が追加、変更、または削除されなかった理由を調べることができます。 **レコード**の**ステータス**が公開されているのみ有効です。**フィールド**コレクションは、**レコード セット**ではありません。**フィールド**のコレクションです。

**Field** を追加、変更、または削除するときに 2 つの問題が発生する可能性があります。ユーザーが **Field** を削除すると、 **Fields** コレクションから削除されたことを示すマークが付けられます。ユーザーが権限を与えられていない **Field** を削除しようとしたために、それ以降の **Update** がエラーを返す場合、 **Field** のステータスは **adFieldPermissionDenied** **OR** **adFieldPendingDelete** になります。 [CancelUpdate](cancelupdate-method-ado.md) メソッドを呼び出すと、元の値が復元され、 **Status** は **adFieldOK** になります。同様に、新規 **Field** が追加され、不適切な値が割り当てられたために、 **Update** メソッドがエラーを返す場合があります。この場合、新規 **Field** は **Fields** コレクションに追加されますが、ステータスは **adFieldPendingInsert** および場合によっては **adFieldCantCreate** になります。新規 **Field** に適切な値を指定し、 **Update** を再度呼び出すことができます。代わりに **Resync** を呼び出すと、プロバイダーに再度クエリが実行されます。

