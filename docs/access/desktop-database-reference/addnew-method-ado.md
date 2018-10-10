---
title: AddNew メソッド (ADO)
TOCTitle: AddNew Method (ADO)
ms:assetid: bae09be0-5707-4f38-9c74-0acd0f29dbac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249899(v=office.15)
ms:contentKeyID: 48547384
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b84e6651093d932a17ff20097841bf84bac00c66
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479188"
---
# <a name="addnew-method-ado"></a><span data-ttu-id="9fc16-102">AddNew メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="9fc16-102">AddNew Method (ADO)</span></span>


<span data-ttu-id="9fc16-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="9fc16-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9fc16-104">更新可能な [Recordset](recordset-object-ado.md) オブジェクトの新しいレコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="9fc16-104">Creates a new record for an updatable [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fc16-105">構文</span><span class="sxs-lookup"><span data-stu-id="9fc16-105">Syntax</span></span>

<span data-ttu-id="9fc16-106">*レコード セット*です。AddNew *FieldList*、*値*</span><span class="sxs-lookup"><span data-stu-id="9fc16-106">*recordset*.AddNew *FieldList*, *Values*</span></span>

## <a name="parameters"></a><span data-ttu-id="9fc16-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9fc16-107">Parameters</span></span>

  - <span data-ttu-id="9fc16-108">*recordset*</span><span class="sxs-lookup"><span data-stu-id="9fc16-108">*recordset*</span></span>

  - <span data-ttu-id="9fc16-109">**Recordset** オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="9fc16-109">A **Recordset** object.</span></span>

  - <span data-ttu-id="9fc16-110">*FieldList*</span><span class="sxs-lookup"><span data-stu-id="9fc16-110">*FieldList*</span></span>

  - <span data-ttu-id="9fc16-p101">省略可能です。新しいレコード内の単一フィールドの名前であるか、複数フィールドの名前または順序の配列です。</span><span class="sxs-lookup"><span data-stu-id="9fc16-p101">Optional. A single name, or an array of names or ordinal positions of the fields in the new record.</span></span>

  - <span data-ttu-id="9fc16-113">*Values*</span><span class="sxs-lookup"><span data-stu-id="9fc16-113">*Values*</span></span>

  - <span data-ttu-id="9fc16-114">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="9fc16-114">Optional.</span></span> <span data-ttu-id="9fc16-115">1 つの値、または新しいレコードのフィールドの値の配列。</span><span class="sxs-lookup"><span data-stu-id="9fc16-115">A single value, or an array of values for the fields in the new record.</span></span> <span data-ttu-id="9fc16-116">*Fieldlist*が配列の場合は、*値*配列と同じ数のメンバーにもする必要があります。それ以外の場合、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="9fc16-116">If *Fieldlist* is an array, *Values* must also be an array with the same number of members; otherwise, an error occurs.</span></span> <span data-ttu-id="9fc16-117">また、一方の配列におけるフィールド名の順序と、もう一方の配列におけるフィールド値の順序は、一致している必要があります。</span><span class="sxs-lookup"><span data-stu-id="9fc16-117">The order of field names must match the order of field values in each array.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fc16-118">解説</span><span class="sxs-lookup"><span data-stu-id="9fc16-118">Remarks</span></span>

<span data-ttu-id="9fc16-p103">**AddNew** メソッドは、新しいレコードの作成と初期化に使用します。現在の [Recordset](supports-method-ado.md) オブジェクトにレコードを追加できるかどうかを確認するには、 **Supports** メソッドに [adAddNew](cursoroptionenum.md) ( **CursorOptionEnum** 値) を指定して使用します。</span><span class="sxs-lookup"><span data-stu-id="9fc16-p103">Use the **AddNew** method to create and initialize a new record. Use the [Supports](supports-method-ado.md) method with **adAddNew** (a [CursorOptionEnum](cursoroptionenum.md) value) to verify whether you can add records to the current **Recordset** object.</span></span>

<span data-ttu-id="9fc16-p104">**AddNew** メソッドを呼び出した後は、新しいレコードがカレント レコードになり、 [Update](update-method-ado.md) メソッドを呼び出した後もカレント レコードのままになります。新しいレコードは **Recordset** の最後に追加されるので、Update に続いて **MoveNext** を呼び出すと、 **Recordset** の末尾を超えて移動し、 **EOF** が True になります。 **Recordset** オブジェクトがブックマークをサポートしていない場合は、別のレコードに移動すると、新しいレコードにアクセスできなくなることがあります。カーソルの種類によっては、新規レコードにアクセスするために、 [Requery](requery-method-ado.md) メソッドを呼び出すことが必要になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="9fc16-p104">After you call the **AddNew** method, the new record becomes the current record and remains current after you call the [Update](update-method-ado.md) method. Since the new record is appended to the **Recordset**, a call to **MoveNext** following the Update will move past the end of the **Recordset**, making **EOF** True. If the **Recordset** object does not support bookmarks, you may not be able to access the new record once you move to another record. Depending on your cursor type, you may need to call the [Requery](requery-method-ado.md) method to make the new record accessible.</span></span>

<span data-ttu-id="9fc16-125">カレント レコードの編集中または新規レコードの追加中に **AddNew** メソッドを呼び出すと、ADO は **Update** メソッドを呼び出してすべての変更を保存した後、新しいレコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="9fc16-125">If you call **AddNew** while editing the current record or while adding a new record, ADO calls the **Update** method to save any changes and then creates the new record.</span></span>

<span data-ttu-id="9fc16-126">**AddNew**メソッドの動作は、**レコード セット**オブジェクトと、 *Fieldlist*と*値*の引数を渡すかどうかの更新モードに依存します。</span><span class="sxs-lookup"><span data-stu-id="9fc16-126">The behavior of the **AddNew** method depends on the updating mode of the **Recordset** object and whether you pass the *Fieldlist* and *Values* arguments.</span></span>

<span data-ttu-id="9fc16-127">*イミディ エイト更新モード*(のプロバイダーに変更を書き込みます基底のデータ ソース**の更新**メソッドを呼び出すと)、 **adEditAdd** ( [EditMode](editmode-property-ado.md)プロパティを設定する引数を指定しないで**AddNew**メソッドを呼び出す[EditModeEnum](editmodeenum.md)値)。</span><span class="sxs-lookup"><span data-stu-id="9fc16-127">In *immediate update mode* (in which the provider writes changes to the underlying data source once you call the **Update** method), calling the **AddNew** method without arguments sets the [EditMode](editmode-property-ado.md) property to **adEditAdd** (an [EditModeEnum](editmodeenum.md) value).</span></span> <span data-ttu-id="9fc16-128">プロバイダーは、ローカルでのフィールド値の変更をキャッシュします。</span><span class="sxs-lookup"><span data-stu-id="9fc16-128">The provider caches any field value changes locally.</span></span> <span data-ttu-id="9fc16-129">**Update**メソッドを呼び出してデータベースに新しいレコードを転記し、 **EditMode**プロパティが**adEditNone** ( **EditModeEnum**値) にリセットします。</span><span class="sxs-lookup"><span data-stu-id="9fc16-129">Calling the **Update** method posts the new record to the database and resets the **EditMode** property to **adEditNone** (an **EditModeEnum** value).</span></span> <span data-ttu-id="9fc16-130">ADO が ( **Update**呼び出し必要はありません)、データベースに新しいレコードをすぐに投稿、 *Fieldlist*と*値*の引数を渡す場合**EditMode**プロパティの値には、(**adEditNone**) は変更されません。</span><span class="sxs-lookup"><span data-stu-id="9fc16-130">If you pass the *Fieldlist* and *Values* arguments, ADO immediately posts the new record to the database (no **Update** call is necessary); the **EditMode** property value does not change (**adEditNone**).</span></span>

<span data-ttu-id="9fc16-131">*バッチ更新モード*(をプロバイダー複数の変更をキャッシュし、 [UpdateBatch](updatebatch-method-ado.md)メソッドを呼び出した場合にのみ、基になるデータ ソースに書き込みます)、 **EditMode**を設定する引数を指定しないで**AddNew**メソッドを呼び出す**adEditAdd**プロパティです。</span><span class="sxs-lookup"><span data-stu-id="9fc16-131">In *batch update mode* (in which the provider caches multiple changes and writes them to the underlying data source only when you call the [UpdateBatch](updatebatch-method-ado.md) method), calling the **AddNew** method without arguments sets the **EditMode** property to **adEditAdd**.</span></span> <span data-ttu-id="9fc16-132">プロバイダーは、ローカルでのフィールド値の変更をキャッシュします。</span><span class="sxs-lookup"><span data-stu-id="9fc16-132">The provider caches any field value changes locally.</span></span> <span data-ttu-id="9fc16-133">**UpdateBatch が呼び出されるまで、プロバイダーは基になるデータベースへの変更 post しないですが、現在の**レコード セット**に新しいレコードを追加します。 **Update**メソッドを呼び出すと、 **EditMode**プロパティが**adEditNone**にリセット**メソッドです。</span><span class="sxs-lookup"><span data-stu-id="9fc16-133">Calling the **Update** method adds the new record to the current **Recordset** and resets the **EditMode** property to **adEditNone**, but the provider does not post the changes to the underlying database until you call the **UpdateBatch** method.</span></span> <span data-ttu-id="9fc16-134">ADO がプロバイダーをキャッシュに格納するために新しいレコードを送信する、 *Fieldlist*と*値*の引数を渡す場合**UpdateBatch**メソッドを呼び出して基になるデータベースに新しいレコードを転記する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9fc16-134">If you pass the *Fieldlist* and *Values* arguments, ADO sends the new record to the provider for storage in a cache; you need to call the **UpdateBatch** method to post the new record to the underlying database.</span></span>
