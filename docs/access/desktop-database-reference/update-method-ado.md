---
title: Update メソッド (ADO)
TOCTitle: Update method (ADO)
ms:assetid: fc88cab6-c379-bb4f-530c-da08107924e0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250294(v=office.15)
ms:contentKeyID: 48548893
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f077634abea6fadfe5c4305fc25b28e6d57bf13e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710637"
---
# <a name="update-method-ado"></a><span data-ttu-id="31b8c-102">Update メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="31b8c-102">Update method (ADO)</span></span>

<span data-ttu-id="31b8c-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="31b8c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="31b8c-104">[Recordset](recordset-object-ado.md) オブジェクトのカレント行、または [Record](fields-collection-ado.md) オブジェクトの [Fields](record-object-ado.md) コレクションに加えた変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="31b8c-104">Saves any changes you make to the current row of a [Recordset](recordset-object-ado.md) object, or the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="31b8c-105">構文</span><span class="sxs-lookup"><span data-stu-id="31b8c-105">Syntax</span></span>

<span data-ttu-id="31b8c-106">*レコード セット*です。*フィールド*、*値*を更新します。</span><span class="sxs-lookup"><span data-stu-id="31b8c-106">*recordset*.Update*Fields*, *Values*</span></span>

<span data-ttu-id="31b8c-107">*レコード*です。</span><span class="sxs-lookup"><span data-stu-id="31b8c-107">*record*.</span></span> <span data-ttu-id="31b8c-108">*フィールド*です。更新</span><span class="sxs-lookup"><span data-stu-id="31b8c-108">*Fields*.Update</span></span>

## <a name="parameters"></a><span data-ttu-id="31b8c-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31b8c-109">Parameters</span></span>

|<span data-ttu-id="31b8c-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31b8c-110">Parameter</span></span>|<span data-ttu-id="31b8c-111">説明</span><span class="sxs-lookup"><span data-stu-id="31b8c-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="31b8c-112">*Fields*</span><span class="sxs-lookup"><span data-stu-id="31b8c-112">*Fields*</span></span> |<span data-ttu-id="31b8c-p102">省略可能です。変更する単一のフィールドの名前を表すバリアント型 ( **Variant** ) の値、または複数のフィールドの名前か順序を表すバリアント型 ( **Variant** ) の配列を指定します。</span><span class="sxs-lookup"><span data-stu-id="31b8c-p102">Optional. A **Variant** that represents a single name, or a **Variant** array that represents names or ordinal positions of the field or fields you wish to modify.</span></span>|
|<span data-ttu-id="31b8c-115">*Values*</span><span class="sxs-lookup"><span data-stu-id="31b8c-115">*Values*</span></span> |<span data-ttu-id="31b8c-p103">省略可能です。新しいレコードでの単一のフィールドの値を表すバリアント型 ( **Variant** ) の値、または複数のフィールドの値を表すバリアント型 ( **Variant** ) の配列を指定します。</span><span class="sxs-lookup"><span data-stu-id="31b8c-p103">Optional. A **Variant** that represents a single value, or a **Variant** array that represents values for the field or fields in the new record.</span></span>|

## <a name="remarks"></a><span data-ttu-id="31b8c-118">解説</span><span class="sxs-lookup"><span data-stu-id="31b8c-118">Remarks</span></span>

### <a name="recordset"></a><span data-ttu-id="31b8c-119">Recordset</span><span class="sxs-lookup"><span data-stu-id="31b8c-119">Recordset</span></span>

<span data-ttu-id="31b8c-p104">**Update** メソッドを使用すると、 **AddNew** メソッドを呼び出したか、または既存レコードのいずれかのフィールドの値を変更した時点以降に [Recordset](addnew-method-ado.md) オブジェクトのカレント レコードに加えた変更がすべて保存されます。 **Recordset** オブジェクトが更新をサポートしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="31b8c-p104">Use the **Update** method to save any changes you make to the current record of a **Recordset** object since calling the [AddNew](addnew-method-ado.md) method or since changing any field values in an existing record. The **Recordset** object must support updates.</span></span>

<span data-ttu-id="31b8c-122">フィールドの値を設定するには、次のいずれかを行います。</span><span class="sxs-lookup"><span data-stu-id="31b8c-122">To set field values, do one of the following:</span></span>

- <span data-ttu-id="31b8c-123">[Field](field-object-ado.md) オブジェクトの [Value](value-property-ado.md) プロパティに値を代入してから、 **Update** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="31b8c-123">Assign values to a [Field](field-object-ado.md) object's [Value](value-property-ado.md) property and call the **Update** method.</span></span>

- <span data-ttu-id="31b8c-124">フィールド名と値を **Update** 呼び出しで引数として渡します。</span><span class="sxs-lookup"><span data-stu-id="31b8c-124">Pass a field name and a value as arguments with the **Update** call.</span></span>

- <span data-ttu-id="31b8c-125">フィールド名の配列と値の配列を **Update** 呼び出しで渡します。</span><span class="sxs-lookup"><span data-stu-id="31b8c-125">Pass an array of field names and an array of values with the **Update** call.</span></span>

<span data-ttu-id="31b8c-p105">フィールドと値の配列を使用する場合は、両方の配列の要素の数を同じにする必要があります。また、フィールド名の順序がフィールドの値の順序と一致している必要があります。フィールドと値の数と順序が一致していないと、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="31b8c-p105">When you use arrays of fields and values, there must be an equal number of elements in both arrays. Also, the order of field names must match the order of field values. If the number and order of fields and values do not match, an error occurs.</span></span>

<span data-ttu-id="31b8c-p106">**Recordset** オブジェクトが一括更新をサポートしている場合は、1 つまたは複数のレコードへの複数の変更をローカルにキャッシュしてから、 [UpdateBatch](updatebatch-method-ado.md) メソッドを呼び出すことができます。カレント レコードの編集中、または新しいレコードの追加中に **UpdateBatch** メソッドを呼び出すと、ADO によって自動的に **Update** メソッドが呼び出されてカレント レコードへの保留中の変更が保存されてから、変更内容がまとめてプロバイダーに転送されます。</span><span class="sxs-lookup"><span data-stu-id="31b8c-p106">If the **Recordset** object supports batch updating, you can cache multiple changes to one or more records locally until you call the [UpdateBatch](updatebatch-method-ado.md) method. If you are editing the current record or adding a new record when you call the **UpdateBatch** method, ADO will automatically call the **Update** method to save any pending changes to the current record before transmitting the batched changes to the provider.</span></span>

<span data-ttu-id="31b8c-p107">**Update** メソッドを呼び出すより前に追加中または編集中のレコードから移動すると、ADO によって自動的に **Update** が呼び出されて変更内容が保存されます。カレント レコードに加えた変更を取り消す場合や、新しく追加したレコードを破棄する場合は、 [CancelUpdate](cancelupdate-method-ado.md) メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="31b8c-p107">If you move from the record you are adding or editing before calling the **Update** method, ADO will automatically call **Update** to save the changes. You must call the [CancelUpdate](cancelupdate-method-ado.md) method if you want to cancel any changes made to the current record or discard a newly added record.</span></span>

<span data-ttu-id="31b8c-133">カレント レコードは、 **Update** メソッドを呼び出した後もカレントのままです。</span><span class="sxs-lookup"><span data-stu-id="31b8c-133">The current record remains current after you call the **Update** method.</span></span>

### <a name="record"></a><span data-ttu-id="31b8c-134">Record</span><span class="sxs-lookup"><span data-stu-id="31b8c-134">Record</span></span>

<span data-ttu-id="31b8c-135">**Update** メソッドは、 [Record](fields-collection-ado.md) オブジェクトの **Fields** コレクションへのフィールドの追加、削除、および更新を完了させます。</span><span class="sxs-lookup"><span data-stu-id="31b8c-135">The **Update** method finalizes additions, deletions, and updates to fields in the [Fields](fields-collection-ado.md) collection of a **Record** object.</span></span>

<span data-ttu-id="31b8c-p108">たとえば、 **Delete** メソッドで削除されたフィールドは、直ちに削除のマークが付けられますが、コレクション内には残されます。これらのフィールドをプロバイダーのコレクションから実際に削除するには、 **Update** メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="31b8c-p108">For example, fields deleted with the **Delete** method are marked for deletion immediately but remain in the collection. The **Update** method must be called to actually delete these fields from the provider's collection.</span></span>

