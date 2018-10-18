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
# <a name="status-property-ado-field"></a><span data-ttu-id="c5516-102">Status プロパティ (ADO Field)</span><span class="sxs-lookup"><span data-stu-id="c5516-102">Status Property (ADO Field)</span></span>


<span data-ttu-id="c5516-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="c5516-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c5516-104">[Field](field-object-ado.md) オブジェクトのステータスを示します。</span><span class="sxs-lookup"><span data-stu-id="c5516-104">Indicates the status of a [Field](field-object-ado.md) object.</span></span>

<span data-ttu-id="c5516-105"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="c5516-105"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="c5516-106">戻り値</span><span class="sxs-lookup"><span data-stu-id="c5516-106">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="c5516-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="c5516-107">Return value</span></span>
>>>>>>> <span data-ttu-id="c5516-108">master</span><span class="sxs-lookup"><span data-stu-id="c5516-108">master</span></span>

<span data-ttu-id="c5516-p101">[FieldStatusEnum](fieldstatusenum.md) 値を返します。既定値は **adFieldOK** です。</span><span class="sxs-lookup"><span data-stu-id="c5516-p101">Returns a [FieldStatusEnum](fieldstatusenum.md) value. The default value is **adFieldOK**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5516-111">解説</span><span class="sxs-lookup"><span data-stu-id="c5516-111">Remarks</span></span>

<span data-ttu-id="c5516-112">**Recordset** オブジェクトのフィールドについては、このプロパティは常に [adFieldOK](recordset-object-ado.md) を返します。</span><span class="sxs-lookup"><span data-stu-id="c5516-112">This property always returns **adFieldOK** for fields of a [Recordset](recordset-object-ado.md) object.</span></span>

<span data-ttu-id="c5516-p102">[Record](fields-collection-ado.md) オブジェクトの [Fields](record-object-ado.md) コレクションに対する追加や削除は、 [Update](update-method-ado.md) メソッドが呼び出されるまでキャッシュされます。 **Status** プロパティを使用すると、正常に追加または削除されたフィールドを特定できます。</span><span class="sxs-lookup"><span data-stu-id="c5516-p102">Additions and deletions to the [Fields](fields-collection-ado.md) collections of the [Record](record-object-ado.md) object are cached until the [Update](update-method-ado.md) method is called. The **Status** property enables you to determine which fields have been successfully added or deleted.</span></span>

<span data-ttu-id="c5516-115">パフォーマンスを向上させるため、スキーマの変更は **Update** が呼び出されるまでキャッシュされ、その変更は共有的バッチ更新で反映されます。</span><span class="sxs-lookup"><span data-stu-id="c5516-115">To enhance performance, schema changes are cached until **Update** is called, and then the changes are made in a batch optimistic update.</span></span> <span data-ttu-id="c5516-116">**Update** メソッドが呼び出されなかった場合、サーバーは更新されません。</span><span class="sxs-lookup"><span data-stu-id="c5516-116">If the **Update** method is not called, the server is not updated.</span></span> <span data-ttu-id="c5516-117">更新に失敗した場合は、エラーが返され、 **Status** プロパティは操作とエラー ステータス コードを組み合わせた値になります。</span><span class="sxs-lookup"><span data-stu-id="c5516-117">If any updates fail then an error is returned and the **Status** property indicates the combined values of the operation and error status code.</span></span> <span data-ttu-id="c5516-118">たとえば、 **adFieldPendingInsert** **OR** **adFieldPermissionDenied** です。</span><span class="sxs-lookup"><span data-stu-id="c5516-118">For example, **adFieldPendingInsert** **OR** **adFieldPermissionDenied**.</span></span> <span data-ttu-id="c5516-119">各 **Field** の **Status** プロパティを使用すると、 **Field** が追加、変更、または削除されなかった理由を調べることができます。</span><span class="sxs-lookup"><span data-stu-id="c5516-119">The **Status** property for each **Field** can be used to determine why the **Field** was not added, modified, or deleted.</span></span> <span data-ttu-id="c5516-120">**レコード**の**ステータス**が公開されているのみ有効です。**フィールド**コレクションは、**レコード セット**ではありません。**フィールド**のコレクションです。</span><span class="sxs-lookup"><span data-stu-id="c5516-120">**Status** is only meaningfully exposed on the **Record**.**Fields** collection and not the **Recordset**.**Fields** collection.</span></span>

<span data-ttu-id="c5516-p104">**Field** を追加、変更、または削除するときに 2 つの問題が発生する可能性があります。ユーザーが **Field** を削除すると、 **Fields** コレクションから削除されたことを示すマークが付けられます。ユーザーが権限を与えられていない **Field** を削除しようとしたために、それ以降の **Update** がエラーを返す場合、 **Field** のステータスは **adFieldPermissionDenied** **OR** **adFieldPendingDelete** になります。 [CancelUpdate](cancelupdate-method-ado.md) メソッドを呼び出すと、元の値が復元され、 **Status** は **adFieldOK** になります。同様に、新規 **Field** が追加され、不適切な値が割り当てられたために、 **Update** メソッドがエラーを返す場合があります。この場合、新規 **Field** は **Fields** コレクションに追加されますが、ステータスは **adFieldPendingInsert** および場合によっては **adFieldCantCreate** になります。新規 **Field** に適切な値を指定し、 **Update** を再度呼び出すことができます。代わりに **Resync** を呼び出すと、プロバイダーに再度クエリが実行されます。</span><span class="sxs-lookup"><span data-stu-id="c5516-p104">Two problems can arise when adding, modifying, or deleting a **Field**. If the user deletes a **Field**, it is marked for deletion from the **Fields** collection. If the subsequent **Update** returns an error because the user tried to delete a **Field** for which they do not have permission, the **Field** will have a status of **adFieldPermissionDenied** **OR** **adFieldPendingDelete**. Calling the [CancelUpdate](cancelupdate-method-ado.md) method restores original values and sets the **Status** to **adFieldOK**. Similarly, the **Update** method may return an error because a new **Field** was added and given an inappropriate value. In that case the new **Field** will be in the **Fields** collection and have a status of **adFieldPendingInsert** and perhaps **adFieldCantCreate**. You can supply an appropriate value for the new **Field** and call **Update** again. Note that calling **Resync** instead requeries the provider.</span></span>

