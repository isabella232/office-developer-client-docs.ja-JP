---
title: UpdateBatch メソッド (ADO)
TOCTitle: UpdateBatch method (ADO)
ms:assetid: 69e72a65-b637-36fd-d09f-7f81050f71ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249416(v=office.15)
ms:contentKeyID: 48545420
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9d269a9012588a7b82505ac2e28466151715cbb0
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706003"
---
# <a name="updatebatch-method-ado"></a><span data-ttu-id="b97ff-102">UpdateBatch メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="b97ff-102">UpdateBatch method (ADO)</span></span>

<span data-ttu-id="b97ff-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="b97ff-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b97ff-104">保留中の一括更新をすべてディスクに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="b97ff-104">Writes all pending batch updates to disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="b97ff-105">構文</span><span class="sxs-lookup"><span data-stu-id="b97ff-105">Syntax</span></span>

<span data-ttu-id="b97ff-106">*レコード セット*です。UpdateBatch*AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="b97ff-106">*recordset*.UpdateBatch*AffectRecords*</span></span>

## <a name="parameters"></a><span data-ttu-id="b97ff-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b97ff-107">Parameters</span></span>

|<span data-ttu-id="b97ff-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b97ff-108">Parameter</span></span>|<span data-ttu-id="b97ff-109">説明</span><span class="sxs-lookup"><span data-stu-id="b97ff-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="b97ff-110">*AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="b97ff-110">*AffectRecords*</span></span> |<span data-ttu-id="b97ff-p101">省略可能です。 [UpdateBatch](affectenum.md) メソッドで処理するレコードの数を示す **AffectEnum** 値を指定します。</span><span class="sxs-lookup"><span data-stu-id="b97ff-p101">Optional. An [AffectEnum](affectenum.md) value that indicates how many records the **UpdateBatch** method will affect.</span></span>|

## <a name="remarks"></a><span data-ttu-id="b97ff-113">解説</span><span class="sxs-lookup"><span data-stu-id="b97ff-113">Remarks</span></span>

<span data-ttu-id="b97ff-114">**Recordset** オブジェクトを一括更新モードで変更している場合に **UpdateBatch** メソッドを使用すると、 **Recordset** オブジェクトに加えられた変更を基になるデータベースに転送できます。</span><span class="sxs-lookup"><span data-stu-id="b97ff-114">Use the **UpdateBatch** method when modifying a **Recordset** object in batch update mode to transmit all changes made in a **Recordset** object to the underlying database.</span></span>

<span data-ttu-id="b97ff-p102">**Recordset** オブジェクトが一括更新をサポートしている場合は、 **UpdateBatch** メソッドを呼び出すまでの間、1 つまたは複数のレコードへの複数の変更をローカルにキャッシュしておくことができます。カレント レコードの編集中、または新しいレコードの追加中に **UpdateBatch** メソッドを呼び出すと、ADO によって自動的に [Update](update-method-ado.md) メソッドが呼び出されてカレント レコードへの保留中の変更が保存されてから、変更内容がまとめてプロバイダーに転送されます。一括更新は、キーセットまたは静的カーソルのみで使用してください。</span><span class="sxs-lookup"><span data-stu-id="b97ff-p102">If the **Recordset** object supports batch updating, you can cache multiple changes to one or more records locally until you call the **UpdateBatch** method. If you are editing the current record or adding a new record when you call the **UpdateBatch** method, ADO will automatically call the [Update](update-method-ado.md) method to save any pending changes to the current record before transmitting the batched changes to the provider. You should use batch updating with either a keyset or static cursor only.</span></span>

> [!NOTE]
> <span data-ttu-id="b97ff-118">[!メモ] パラメーターの値として **adAffectGroup** を指定すると、現在の **Recordset** 内に表示可能なレコードがなかった場合 (一致するレコードのないフィルターがかかっているなど) にはエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="b97ff-118">Specifying **adAffectGroup** as the value for this parameter will result in an error when there are no visible records in the current **Recordset** (such as a filter for which no records match).</span></span>

<span data-ttu-id="b97ff-p103">基になるデータとの競合が原因で一部またはすべてのレコードの変更の転送に失敗した場合 (たとえば、レコードが他のユーザーによって既に削除されていた場合)、プロバイダーから [Errors](errors-collection-ado.md) コレクションに警告が返され、実行時エラーが発生します。[Filter](filter-property-ado.md) プロパティ (**adFilterAffectedRecords**) と [Status](status-property-ado-recordset.md) プロパティを使用すると、競合のあるレコードを突き止めることができます。</span><span class="sxs-lookup"><span data-stu-id="b97ff-p103">If the attempt to transmit changes fails for any or all records because of a conflict with the underlying data (for example, a record has already been deleted by another user), the provider returns warnings to the [Errors](errors-collection-ado.md) collection and a run-time error occurs. Use the [Filter](filter-property-ado.md) property (**adFilterAffectedRecords**) and the [Status](status-property-ado-recordset.md) property to locate records with conflicts.</span></span>

<span data-ttu-id="b97ff-121">保留になっているすべての一括更新を取り消すには、[CancelBatch](cancelbatch-method-ado.md) メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="b97ff-121">To cancel all pending batch updates, use the [CancelBatch](cancelbatch-method-ado.md) method.</span></span>

<span data-ttu-id="b97ff-122">動的プロパティの [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) と [Update Resync](update-resync-property-dynamic-ado.md) が設定されていて、 **Recordset** が複数のテーブルに対して JOIN 操作を実行した結果になっている場合は、 **UpdateBatch** メソッドの実行の後に、 [Update Resync](resync-method-ado.md) プロパティの設定に応じて暗黙的に **Resync** メソッドが実行されます。</span><span class="sxs-lookup"><span data-stu-id="b97ff-122">If the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) and [Update Resync](update-resync-property-dynamic-ado.md) dynamic properties are set, and the **Recordset** is the result of executing a JOIN operation on multiple tables, then the execution of the **UpdateBatch** method is implicitly followed by the [Resync](resync-method-ado.md) method depending on the settings of the **Update Resync** property.</span></span>

<span data-ttu-id="b97ff-p104">個々の一括更新がデータ ソースに対して実行される順序は、必ずしもそれらがローカル **Recordset** に実行された順序と同じになるわけではありません。更新の順序は、プロバイダーに依存します。挿入または更新に対する外部キー制約など、相互に関連のある更新をコーディングする場合は、このことを考慮してください。</span><span class="sxs-lookup"><span data-stu-id="b97ff-p104">The order in which the individual updates of a batch are performed on the data source is not necessarily the same as the order in which they were performed on the local **Recordset**. Update order is dependent upon the provider. Take this into account when coding updates that are related to one another, such as foreign key constraints on an insert or update.</span></span>

