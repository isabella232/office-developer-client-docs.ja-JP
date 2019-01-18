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
# <a name="delete-method-ado-recordset"></a><span data-ttu-id="81efc-102">Delete メソッド (ADO Recordset)</span><span class="sxs-lookup"><span data-stu-id="81efc-102">Delete method (ADO Recordset)</span></span>

<span data-ttu-id="81efc-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="81efc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="81efc-104">カレント レコードまたはレコードのグループを削除します。</span><span class="sxs-lookup"><span data-stu-id="81efc-104">Deletes the current record or a group of records.</span></span>

## <a name="syntax"></a><span data-ttu-id="81efc-105">構文</span><span class="sxs-lookup"><span data-stu-id="81efc-105">Syntax</span></span>

<span data-ttu-id="81efc-106">*レコード セット*です。*AffectRecords*を削除します。</span><span class="sxs-lookup"><span data-stu-id="81efc-106">*recordset*.Delete *AffectRecords*</span></span>

## <a name="parameters"></a><span data-ttu-id="81efc-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="81efc-107">Parameters</span></span>

|<span data-ttu-id="81efc-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="81efc-108">Parameter</span></span>|<span data-ttu-id="81efc-109">説明</span><span class="sxs-lookup"><span data-stu-id="81efc-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="81efc-110">*AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="81efc-110">*AffectRecords*</span></span> |<span data-ttu-id="81efc-p101">[Delete](affectenum.md) メソッドで操作するレコードの数を決める **AffectEnum** 値を指定します。既定値は **adAffectCurrent** です。</span><span class="sxs-lookup"><span data-stu-id="81efc-p101">An [AffectEnum](affectenum.md) value that determines how many records the **Delete** method will affect. The default value is **adAffectCurrent**.</span></span>|

> [!NOTE]
> <span data-ttu-id="81efc-113">[!メモ] **adAffectAll** と **adAffectAllChapters** は、 **Delete** では無効な引数です。</span><span class="sxs-lookup"><span data-stu-id="81efc-113">**adAffectAll** and **adAffectAllChapters** are not valid arguments to **Delete**.</span></span>

## <a name="remarks"></a><span data-ttu-id="81efc-114">解説</span><span class="sxs-lookup"><span data-stu-id="81efc-114">Remarks</span></span>

<span data-ttu-id="81efc-p102">**Delete** メソッドを使用すると、 [Recordset](recordset-object-ado.md) オブジェクト内のカレント レコードまたはレコードのグループは削除の対象としてマークされます。レコードを削除できない **Recordset** オブジェクトの場合は、エラーが発生します。即時更新モードでは、削除は直ちにデータベースに反映されます。データベースの整合性違反などにより削除を実行できない場合、レコードは **Update** を呼び出した後も編集モードのままになります。そのため、 [Close](cancelupdate-method-ado.md)、[Move](close-method-ado.md)、[NextRecordset](move-method-ado.md) などによりカレント レコードから移動する前に、 [CancelUpdate](nextrecordset-method-ado.md) を使用して更新を取り消す必要があります。</span><span class="sxs-lookup"><span data-stu-id="81efc-p102">Using the **Delete** method marks the current record or a group of records in a [Recordset](recordset-object-ado.md) object for deletion. If the **Recordset** object doesn't allow record deletion, an error occurs. If you are in immediate update mode, deletions occur in the database immediately. If a record cannot be successfully deleted (due to database integrity violations, for example), the record will remain in edit mode after the call to **Update**. This means that you must cancel the update with [CancelUpdate](cancelupdate-method-ado.md) before moving off the current record (for example, with [Close](close-method-ado.md), [Move](move-method-ado.md), or [NextRecordset](nextrecordset-method-ado.md)).</span></span>

<span data-ttu-id="81efc-p103">バッチ更新モードでは、キャッシュ内の削除されるレコードにマークはされますが、実際の削除は [UpdateBatch](updatebatch-method-ado.md) メソッドを呼び出すまで行われません。削除されたレコードを参照するには、 [Filter](filter-property-ado.md) プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="81efc-p103">If you are in batch update mode, the records are marked for deletion from the cache and the actual deletion happens when you call the [UpdateBatch](updatebatch-method-ado.md) method. (Use the [Filter](filter-property-ado.md) property to view the deleted records.)</span></span>

<span data-ttu-id="81efc-p104">削除されたレコードからフィールド値を取得すると、エラーが発生します。カレント レコードを削除すると、別のレコードに移動するまで、削除されたレコードがカレント レコードのままになります。削除されたレコードから移動した後は、そのレコードにアクセスできなくなります。</span><span class="sxs-lookup"><span data-stu-id="81efc-p104">Retrieving field values from the deleted record generates an error. After deleting the current record, the deleted record remains current until you move to a different record. Once you move away from the deleted record, it is no longer accessible.</span></span>

<span data-ttu-id="81efc-p105">トランザクションで削除レコードをネストしている場合は、[RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) メソッドを使用して、削除されたレコードを復元することができます。バッチ更新モードの場合は、保留中の削除を [CancelBatch](cancelbatch-method-ado.md) メソッドで取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="81efc-p105">If you nest deletions in a transaction, you can recover deleted records with the [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) method. If you are in batch update mode, you can cancel a pending deletion or group of pending deletions with the [CancelBatch](cancelbatch-method-ado.md) method.</span></span>

<span data-ttu-id="81efc-p106">基になるデータとの競合 (レコードが別のユーザーによって既に削除されているなど) が原因でレコードの削除が失敗した場合は、プロバイダーから [Errors](errors-collection-ado.md) コレクションに警告が返されますが、プログラムの実行は停止されません。実行時エラーが発生するのは、要求したすべてのレコードで競合が発生した場合のみです。</span><span class="sxs-lookup"><span data-stu-id="81efc-p106">If the attempt to delete records fails because of a conflict with the underlying data (for example, a record has already been deleted by another user), the provider returns warnings to the [Errors](errors-collection-ado.md) collection but does not halt program execution. A run-time error occurs only if there are conflicts on all the requested records.</span></span>

<span data-ttu-id="81efc-129">[Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) ダイナミック プロパティが設定されていて、 **Recordset** が複数のテーブルに対して JOIN 操作を実行した結果である場合、 **Delete** メソッドは、 [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) プロパティで指定されたテーブルからのみ行を削除できます。</span><span class="sxs-lookup"><span data-stu-id="81efc-129">If the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) dynamic property is set, and the **Recordset** is the result of executing a JOIN operation on multiple tables, then the **Delete** method will only delete rows from the table named in the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) property.</span></span>

