---
title: Delete メソッド (ADO Recordset)
TOCTitle: Delete method (ADO Recordset)
ms:assetid: 62c39b4d-223e-7b48-6780-6cd272e3114e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249374(v=office.15)
ms:contentKeyID: 48545246
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e8142d4fc4fc0036f80693f0bff779d9f3f2a62e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702489"
---
# <a name="delete-method-ado-recordset"></a>Delete メソッド (ADO Recordset)

**適用されます**Access 2013、Office 2013。

カレント レコードまたはレコードのグループを削除します。

## <a name="syntax"></a>構文

*レコード セット*です。*AffectRecords*を削除します。

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*AffectRecords* |[Delete](affectenum.md) メソッドで操作するレコードの数を決める **AffectEnum** 値を指定します。既定値は **adAffectCurrent** です。|

> [!NOTE]
> [!メモ] **adAffectAll** と **adAffectAllChapters** は、 **Delete** では無効な引数です。

## <a name="remarks"></a>解説

**Delete** メソッドを使用すると、 [Recordset](recordset-object-ado.md) オブジェクト内のカレント レコードまたはレコードのグループは削除の対象としてマークされます。レコードを削除できない **Recordset** オブジェクトの場合は、エラーが発生します。即時更新モードでは、削除は直ちにデータベースに反映されます。データベースの整合性違反などにより削除を実行できない場合、レコードは **Update** を呼び出した後も編集モードのままになります。そのため、 [Close](cancelupdate-method-ado.md)、[Move](close-method-ado.md)、[NextRecordset](move-method-ado.md) などによりカレント レコードから移動する前に、 [CancelUpdate](nextrecordset-method-ado.md) を使用して更新を取り消す必要があります。

バッチ更新モードでは、キャッシュ内の削除されるレコードにマークはされますが、実際の削除は [UpdateBatch](updatebatch-method-ado.md) メソッドを呼び出すまで行われません。削除されたレコードを参照するには、 [Filter](filter-property-ado.md) プロパティを使用します。

削除されたレコードからフィールド値を取得すると、エラーが発生します。カレント レコードを削除すると、別のレコードに移動するまで、削除されたレコードがカレント レコードのままになります。削除されたレコードから移動した後は、そのレコードにアクセスできなくなります。

トランザクションで削除レコードをネストしている場合は、[RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) メソッドを使用して、削除されたレコードを復元することができます。バッチ更新モードの場合は、保留中の削除を [CancelBatch](cancelbatch-method-ado.md) メソッドで取り消すことができます。

基になるデータとの競合 (レコードが別のユーザーによって既に削除されているなど) が原因でレコードの削除が失敗した場合は、プロバイダーから [Errors](errors-collection-ado.md) コレクションに警告が返されますが、プログラムの実行は停止されません。実行時エラーが発生するのは、要求したすべてのレコードで競合が発生した場合のみです。

[Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) ダイナミック プロパティが設定されていて、 **Recordset** が複数のテーブルに対して JOIN 操作を実行した結果である場合、 **Delete** メソッドは、 [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) プロパティで指定されたテーブルからのみ行を削除できます。

