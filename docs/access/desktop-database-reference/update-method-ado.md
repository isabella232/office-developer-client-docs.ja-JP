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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306238"
---
# <a name="update-method-ado"></a><span data-ttu-id="ca7cf-102">Update メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="ca7cf-102">Update method (ADO)</span></span>

<span data-ttu-id="ca7cf-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="ca7cf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ca7cf-104">[Recordset](recordset-object-ado.md) オブジェクトのカレント行、または [Record](record-object-ado.md) オブジェクトの [Fields](fields-collection-ado.md) コレクションに加えた変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="ca7cf-104">Saves any changes you make to the current row of a [Recordset](recordset-object-ado.md) object, or the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca7cf-105">構文</span><span class="sxs-lookup"><span data-stu-id="ca7cf-105">Syntax</span></span>

<span data-ttu-id="ca7cf-106">*recordset*。*フィールド*、*値*を更新する</span><span class="sxs-lookup"><span data-stu-id="ca7cf-106">*recordset*.Update*Fields*, *Values*</span></span>

<span data-ttu-id="ca7cf-107">*レコード*。</span><span class="sxs-lookup"><span data-stu-id="ca7cf-107">*record*.</span></span> <span data-ttu-id="ca7cf-108">*フィールド*。更新</span><span class="sxs-lookup"><span data-stu-id="ca7cf-108">*Fields*.Update</span></span>

## <a name="parameters"></a><span data-ttu-id="ca7cf-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ca7cf-109">Parameters</span></span>

|<span data-ttu-id="ca7cf-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ca7cf-110">Parameter</span></span>|<span data-ttu-id="ca7cf-111">説明</span><span class="sxs-lookup"><span data-stu-id="ca7cf-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="ca7cf-112">*Fields*</span><span class="sxs-lookup"><span data-stu-id="ca7cf-112">*Fields*</span></span> |<span data-ttu-id="ca7cf-p102">省略可能です。変更する単一のフィールドの名前を表すバリアント型 ( **Variant** ) の値、または複数のフィールドの名前か順序を表すバリアント型 ( **Variant** ) の配列を指定します。</span><span class="sxs-lookup"><span data-stu-id="ca7cf-p102">Optional. A **Variant** that represents a single name, or a **Variant** array that represents names or ordinal positions of the field or fields you wish to modify.</span></span>|
|<span data-ttu-id="ca7cf-115">*Values*</span><span class="sxs-lookup"><span data-stu-id="ca7cf-115">*Values*</span></span> |<span data-ttu-id="ca7cf-p103">省略可能です。新しいレコードでの単一のフィールドの値を表すバリアント型 ( **Variant** ) の値、または複数のフィールドの値を表すバリアント型 ( **Variant** ) の配列を指定します。</span><span class="sxs-lookup"><span data-stu-id="ca7cf-p103">Optional. A **Variant** that represents a single value, or a **Variant** array that represents values for the field or fields in the new record.</span></span>|

## <a name="remarks"></a><span data-ttu-id="ca7cf-118">注釈</span><span class="sxs-lookup"><span data-stu-id="ca7cf-118">Remarks</span></span>

### <a name="recordset"></a><span data-ttu-id="ca7cf-119">Recordset</span><span class="sxs-lookup"><span data-stu-id="ca7cf-119">Recordset</span></span>

<span data-ttu-id="ca7cf-p104">**Update** メソッドを使用すると、 **AddNew** メソッドを呼び出したか、または既存レコードのいずれかのフィールドの値を変更した時点以降に [Recordset](addnew-method-ado.md) オブジェクトのカレント レコードに加えた変更がすべて保存されます。 **Recordset** オブジェクトが更新をサポートしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="ca7cf-p104">Use the **Update** method to save any changes you make to the current record of a **Recordset** object since calling the [AddNew](addnew-method-ado.md) method or since changing any field values in an existing record. The **Recordset** object must support updates.</span></span>

<span data-ttu-id="ca7cf-122">フィールドの値を設定するには、次のいずれかを行います。</span><span class="sxs-lookup"><span data-stu-id="ca7cf-122">To set field values, do one of the following:</span></span>

- <span data-ttu-id="ca7cf-123">[Field](field-object-ado.md) オブジェクトの [Value](value-property-ado.md) プロパティに値を代入してから、 **Update** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ca7cf-123">Assign values to a [Field](field-object-ado.md) object's [Value](value-property-ado.md) property and call the **Update** method.</span></span>

- <span data-ttu-id="ca7cf-124">フィールド名と値を **Update** 呼び出しで引数として渡します。</span><span class="sxs-lookup"><span data-stu-id="ca7cf-124">Pass a field name and a value as arguments with the **Update** call.</span></span>

- <span data-ttu-id="ca7cf-125">フィールド名の配列と値の配列を **Update** 呼び出しで渡します。</span><span class="sxs-lookup"><span data-stu-id="ca7cf-125">Pass an array of field names and an array of values with the **Update** call.</span></span>

<span data-ttu-id="ca7cf-p105">フィールドと値の配列を使用する場合は、両方の配列の要素の数を同じにする必要があります。また、フィールド名の順序がフィールドの値の順序と一致している必要があります。フィールドと値の数と順序が一致していないと、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="ca7cf-p105">When you use arrays of fields and values, there must be an equal number of elements in both arrays. Also, the order of field names must match the order of field values. If the number and order of fields and values do not match, an error occurs.</span></span>

<span data-ttu-id="ca7cf-p106">**Recordset** オブジェクトが一括更新をサポートしている場合は、1 つまたは複数のレコードへの複数の変更をローカルにキャッシュしてから、 [UpdateBatch](updatebatch-method-ado.md) メソッドを呼び出すことができます。カレント レコードの編集中、または新しいレコードの追加中に **UpdateBatch** メソッドを呼び出すと、ADO によって自動的に **Update** メソッドが呼び出されてカレント レコードへの保留中の変更が保存されてから、変更内容がまとめてプロバイダーに転送されます。</span><span class="sxs-lookup"><span data-stu-id="ca7cf-p106">If the **Recordset** object supports batch updating, you can cache multiple changes to one or more records locally until you call the [UpdateBatch](updatebatch-method-ado.md) method. If you are editing the current record or adding a new record when you call the **UpdateBatch** method, ADO will automatically call the **Update** method to save any pending changes to the current record before transmitting the batched changes to the provider.</span></span>

<span data-ttu-id="ca7cf-p107">**Update** メソッドを呼び出すより前に追加中または編集中のレコードから移動すると、ADO によって自動的に **Update** が呼び出されて変更内容が保存されます。カレント レコードに加えた変更を取り消す場合や、新しく追加したレコードを破棄する場合は、 [CancelUpdate](cancelupdate-method-ado.md) メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="ca7cf-p107">If you move from the record you are adding or editing before calling the **Update** method, ADO will automatically call **Update** to save the changes. You must call the [CancelUpdate](cancelupdate-method-ado.md) method if you want to cancel any changes made to the current record or discard a newly added record.</span></span>

<span data-ttu-id="ca7cf-133">カレント レコードは、 **Update** メソッドを呼び出した後もカレントのままです。</span><span class="sxs-lookup"><span data-stu-id="ca7cf-133">The current record remains current after you call the **Update** method.</span></span>

### <a name="record"></a><span data-ttu-id="ca7cf-134">Record</span><span class="sxs-lookup"><span data-stu-id="ca7cf-134">Record</span></span>

<span data-ttu-id="ca7cf-135">**Update** メソッドは、**Record** オブジェクトの [Fields](fields-collection-ado.md) コレクションへのフィールドの追加、削除、および更新を完了させます。</span><span class="sxs-lookup"><span data-stu-id="ca7cf-135">The **Update** method finalizes additions, deletions, and updates to fields in the [Fields](fields-collection-ado.md) collection of a **Record** object.</span></span>

<span data-ttu-id="ca7cf-p108">たとえば、 **Delete** メソッドで削除されたフィールドは、直ちに削除のマークが付けられますが、コレクション内には残されます。これらのフィールドをプロバイダーのコレクションから実際に削除するには、 **Update** メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="ca7cf-p108">For example, fields deleted with the **Delete** method are marked for deletion immediately but remain in the collection. The **Update** method must be called to actually delete these fields from the provider's collection.</span></span>

