---
title: Update メソッド (ADO)
TOCTitle: Update Method (ADO)
ms:assetid: fc88cab6-c379-bb4f-530c-da08107924e0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250294(v=office.15)
ms:contentKeyID: 48548893
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 772602b31f83d2255c9fdf1b08fa41541f5fc4da
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884108"
---
# <a name="update-method-ado"></a><span data-ttu-id="0c6b7-102">Update メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="0c6b7-102">Update Method (ADO)</span></span>


<span data-ttu-id="0c6b7-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="0c6b7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0c6b7-104">[Recordset](recordset-object-ado.md) オブジェクトのカレント行、または [Record](fields-collection-ado.md) オブジェクトの [Fields](record-object-ado.md) コレクションに加えた変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="0c6b7-104">Saves any changes you make to the current row of a [Recordset](recordset-object-ado.md) object, or the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c6b7-105">構文</span><span class="sxs-lookup"><span data-stu-id="0c6b7-105">Syntax</span></span>

<span data-ttu-id="0c6b7-106">*レコード セット*です。*フィールド*、*値*を更新します。</span><span class="sxs-lookup"><span data-stu-id="0c6b7-106">*recordset*.Update*Fields*, *Values*</span></span>

<span data-ttu-id="0c6b7-107">*レコード*です。</span><span class="sxs-lookup"><span data-stu-id="0c6b7-107">*record*.</span></span> <span data-ttu-id="0c6b7-108">*フィールド*です。更新</span><span class="sxs-lookup"><span data-stu-id="0c6b7-108">*Fields*.Update</span></span>

## <a name="parameters"></a><span data-ttu-id="0c6b7-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0c6b7-109">Parameters</span></span>

  - <span data-ttu-id="0c6b7-110">*Fields*</span><span class="sxs-lookup"><span data-stu-id="0c6b7-110">*Fields*</span></span>

  - <span data-ttu-id="0c6b7-p102">省略可能です。変更する単一のフィールドの名前を表すバリアント型 ( **Variant** ) の値、または複数のフィールドの名前か順序を表すバリアント型 ( **Variant** ) の配列を指定します。</span><span class="sxs-lookup"><span data-stu-id="0c6b7-p102">Optional. A **Variant** that represents a single name, or a **Variant** array that represents names or ordinal positions of the field or fields you wish to modify.</span></span>

  - <span data-ttu-id="0c6b7-113">*Values*</span><span class="sxs-lookup"><span data-stu-id="0c6b7-113">*Values*</span></span>

  - <span data-ttu-id="0c6b7-p103">省略可能です。新しいレコードでの単一のフィールドの値を表すバリアント型 ( **Variant** ) の値、または複数のフィールドの値を表すバリアント型 ( **Variant** ) の配列を指定します。</span><span class="sxs-lookup"><span data-stu-id="0c6b7-p103">Optional. A **Variant** that represents a single value, or a **Variant** array that represents values for the field or fields in the new record.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c6b7-116">解説</span><span class="sxs-lookup"><span data-stu-id="0c6b7-116">Remarks</span></span>

<span data-ttu-id="0c6b7-117">**Recordset**</span><span class="sxs-lookup"><span data-stu-id="0c6b7-117">**Recordset**</span></span>

<span data-ttu-id="0c6b7-p104">**Update** メソッドを使用すると、 **AddNew** メソッドを呼び出したか、または既存レコードのいずれかのフィールドの値を変更した時点以降に [Recordset](addnew-method-ado.md) オブジェクトのカレント レコードに加えた変更がすべて保存されます。 **Recordset** オブジェクトが更新をサポートしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="0c6b7-p104">Use the **Update** method to save any changes you make to the current record of a **Recordset** object since calling the [AddNew](addnew-method-ado.md) method or since changing any field values in an existing record. The **Recordset** object must support updates.</span></span>

<span data-ttu-id="0c6b7-120">フィールドの値を設定するには、次のいずれかを行います。</span><span class="sxs-lookup"><span data-stu-id="0c6b7-120">To set field values, do one of the following:</span></span>

  - <span data-ttu-id="0c6b7-121">[Field](field-object-ado.md) オブジェクトの [Value](value-property-ado.md) プロパティに値を代入してから、 **Update** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0c6b7-121">Assign values to a [Field](field-object-ado.md) object's [Value](value-property-ado.md) property and call the **Update** method.</span></span>

  - <span data-ttu-id="0c6b7-122">フィールド名と値を **Update** 呼び出しで引数として渡します。</span><span class="sxs-lookup"><span data-stu-id="0c6b7-122">Pass a field name and a value as arguments with the **Update** call.</span></span>

  - <span data-ttu-id="0c6b7-123">フィールド名の配列と値の配列を **Update** 呼び出しで渡します。</span><span class="sxs-lookup"><span data-stu-id="0c6b7-123">Pass an array of field names and an array of values with the **Update** call.</span></span>

<span data-ttu-id="0c6b7-p105">フィールドと値の配列を使用する場合は、両方の配列の要素の数を同じにする必要があります。また、フィールド名の順序がフィールドの値の順序と一致している必要があります。フィールドと値の数と順序が一致していないと、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="0c6b7-p105">When you use arrays of fields and values, there must be an equal number of elements in both arrays. Also, the order of field names must match the order of field values. If the number and order of fields and values do not match, an error occurs.</span></span>

<span data-ttu-id="0c6b7-p106">**Recordset** オブジェクトが一括更新をサポートしている場合は、1 つまたは複数のレコードへの複数の変更をローカルにキャッシュしてから、 [UpdateBatch](updatebatch-method-ado.md) メソッドを呼び出すことができます。カレント レコードの編集中、または新しいレコードの追加中に **UpdateBatch** メソッドを呼び出すと、ADO によって自動的に **Update** メソッドが呼び出されてカレント レコードへの保留中の変更が保存されてから、変更内容がまとめてプロバイダーに転送されます。</span><span class="sxs-lookup"><span data-stu-id="0c6b7-p106">If the **Recordset** object supports batch updating, you can cache multiple changes to one or more records locally until you call the [UpdateBatch](updatebatch-method-ado.md) method. If you are editing the current record or adding a new record when you call the **UpdateBatch** method, ADO will automatically call the **Update** method to save any pending changes to the current record before transmitting the batched changes to the provider.</span></span>

<span data-ttu-id="0c6b7-p107">**Update** メソッドを呼び出すより前に追加中または編集中のレコードから移動すると、ADO によって自動的に **Update** が呼び出されて変更内容が保存されます。カレント レコードに加えた変更を取り消す場合や、新しく追加したレコードを破棄する場合は、 [CancelUpdate](cancelupdate-method-ado.md) メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="0c6b7-p107">If you move from the record you are adding or editing before calling the **Update** method, ADO will automatically call **Update** to save the changes. You must call the [CancelUpdate](cancelupdate-method-ado.md) method if you want to cancel any changes made to the current record or discard a newly added record.</span></span>

<span data-ttu-id="0c6b7-131">カレント レコードは、 **Update** メソッドを呼び出した後もカレントのままです。</span><span class="sxs-lookup"><span data-stu-id="0c6b7-131">The current record remains current after you call the **Update** method.</span></span>

<span data-ttu-id="0c6b7-132">**Record**</span><span class="sxs-lookup"><span data-stu-id="0c6b7-132">**Record**</span></span>

<span data-ttu-id="0c6b7-133">**Update** メソッドは、 [Record](fields-collection-ado.md) オブジェクトの **Fields** コレクションへのフィールドの追加、削除、および更新を完了させます。</span><span class="sxs-lookup"><span data-stu-id="0c6b7-133">The **Update** method finalizes additions, deletions, and updates to fields in the [Fields](fields-collection-ado.md) collection of a **Record** object.</span></span>

<span data-ttu-id="0c6b7-p108">たとえば、 **Delete** メソッドで削除されたフィールドは、直ちに削除のマークが付けられますが、コレクション内には残されます。これらのフィールドをプロバイダーのコレクションから実際に削除するには、 **Update** メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="0c6b7-p108">For example, fields deleted with the **Delete** method are marked for deletion immediately but remain in the collection. The **Update** method must be called to actually delete these fields from the provider's collection.</span></span>

