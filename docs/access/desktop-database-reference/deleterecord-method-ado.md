---
title: DeleteRecord メソッド (ADO)
TOCTitle: DeleteRecord method (ADO)
ms:assetid: ba71187f-e580-bba8-f41b-bedfa0bc2b04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249895(v=office.15)
ms:contentKeyID: 48547370
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 69cd8a265688db56d3685c1b2e03bc1c1db6a785
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922798"
---
# <a name="deleterecord-method-ado"></a><span data-ttu-id="c105c-102">DeleteRecord メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="c105c-102">DeleteRecord method (ADO)</span></span>


<span data-ttu-id="c105c-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="c105c-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="c105c-104">[Record](record-object-ado.md) で表されるエンティティを削除します。</span><span class="sxs-lookup"><span data-stu-id="c105c-104">Deletes a the entity represented by a [Record](record-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c105c-105">構文</span><span class="sxs-lookup"><span data-stu-id="c105c-105">Syntax</span></span>

<span data-ttu-id="c105c-106">*レコード\*\*\*関係する。 ソース*、*非同期*。</span><span class="sxs-lookup"><span data-stu-id="c105c-106">*Record*.\**DeleteRecord\*\*\*Source*, *Async*</span></span>

## <a name="parameters"></a><span data-ttu-id="c105c-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c105c-107">Parameters</span></span>

  - <span data-ttu-id="c105c-108">*Source*</span><span class="sxs-lookup"><span data-stu-id="c105c-108">*Source*</span></span>

  - <span data-ttu-id="c105c-p101">省略可能です。削除するエンティティ (ファイル、ディレクトリなど) を表す URL を含む文字列型 (**String**) の値を指定します。*Source* を省略するか、または空の文字列を指定した場合、現在 [Record](record-object-ado.md) で表されているエンティティが削除されます。Record がコレクション レコード (ディレクトリなど、[RecordType](recordtype-property-ado.md) が **adCollectionRecord** であるもの) である場合は、すべての子 (サブディレクトリなど) も削除されます。</span><span class="sxs-lookup"><span data-stu-id="c105c-p101">Optional. A **String** value that contains a URL identifying the entity (for example, the file or directory) to be deleted. If *Source* is omitted or specifies an empty string, the entity represented by the current [Record](record-object-ado.md) is deleted. If the Record is a collection record ([RecordType](recordtype-property-ado.md) of **adCollectionRecord**, such as a directory) all children (for example, subdirectories) will also be deleted.</span></span>

  - <span data-ttu-id="c105c-113">*Async*</span><span class="sxs-lookup"><span data-stu-id="c105c-113">*Async*</span></span>

  - <span data-ttu-id="c105c-p102">省略可能です。ブール型 ( **Boolean** ) の値を指定します。 **True** のときは、削除操作が非同期で実行されることを示します。</span><span class="sxs-lookup"><span data-stu-id="c105c-p102">Optional. A **Boolean** value that, when **True**, specifies that the delete operation is asynchronous.</span></span>

## <a name="remarks"></a><span data-ttu-id="c105c-116">解説</span><span class="sxs-lookup"><span data-stu-id="c105c-116">Remarks</span></span>

<span data-ttu-id="c105c-p103">このメソッドの終了後、 **Record** で表されているオブジェクトに対する操作が失敗する場合があります。 **DeleteRecord** を呼び出した後は **Record** を閉じる必要があります。これは、プロバイダーがデータ ソースで **Record** をいつ更新するかにより、 **Record** の動作が予期できなくなることがあるためです。</span><span class="sxs-lookup"><span data-stu-id="c105c-p103">Operations on the object represented by this **Record** may fail after this method completes. After calling **DeleteRecord**, the **Record** should be closed because the behavior of the **Record** may become unpredictable depending upon when the provider updates the **Record** with the data source.</span></span>

<span data-ttu-id="c105c-119">この**レコード**を[レコード セット](recordset-object-ado.md)から取得した場合、この操作の結果は反映されませんすぐに**レコード セット**で。</span><span class="sxs-lookup"><span data-stu-id="c105c-119">If this **Record** was obtained from a [Recordset](recordset-object-ado.md), then the results of this operation will not be reflected immediately in the **Recordset**.</span></span> <span data-ttu-id="c105c-120">閉じて、再度開いたとき、または**レコード セット**は、[クエリを再実行](requery-method-ado.md)、または[更新](update-method-ado.md)し、[再同期](resync-method-ado.md)の方法を実行することによって、**レコード セット**を更新します。</span><span class="sxs-lookup"><span data-stu-id="c105c-120">Refresh the **Recordset** by closing and re-opening it, or by executing the **Recordset** [Requery](requery-method-ado.md), or [Update](update-method-ado.md) and [Resync](resync-method-ado.md) methods.</span></span>


> [!NOTE]
> <span data-ttu-id="c105c-121">[!メモ] http 体系を使用している URL は、[Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) を自動的に呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c105c-121">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="c105c-122">詳細については、[絶対と相対 Url](absolute-and-relative-urls.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c105c-122">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


