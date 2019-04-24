---
title: DeleteRecord メソッド (ADO)
TOCTitle: DeleteRecord method (ADO)
ms:assetid: ba71187f-e580-bba8-f41b-bedfa0bc2b04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249895(v=office.15)
ms:contentKeyID: 48547370
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8d6ecd408bc2141ef9ff4bec8f6469a70e09bbe1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293995"
---
# <a name="deleterecord-method-ado"></a><span data-ttu-id="07fa5-102">DeleteRecord メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="07fa5-102">DeleteRecord method (ADO)</span></span>

<span data-ttu-id="07fa5-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="07fa5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="07fa5-104">[Record](record-object-ado.md) で表されるエンティティを削除します。</span><span class="sxs-lookup"><span data-stu-id="07fa5-104">Deletes a the entity represented by a [Record](record-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="07fa5-105">構文</span><span class="sxs-lookup"><span data-stu-id="07fa5-105">Syntax</span></span>

<span data-ttu-id="07fa5-106">*Record*. \**DeleteRecord \* \* \* ソース*,*非同期*</span><span class="sxs-lookup"><span data-stu-id="07fa5-106">*Record*.\**DeleteRecord\*\*\*Source*, *Async*</span></span>

## <a name="parameters"></a><span data-ttu-id="07fa5-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07fa5-107">Parameters</span></span>

|<span data-ttu-id="07fa5-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07fa5-108">Parameter</span></span>|<span data-ttu-id="07fa5-109">説明</span><span class="sxs-lookup"><span data-stu-id="07fa5-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="07fa5-110">*Source*</span><span class="sxs-lookup"><span data-stu-id="07fa5-110">*Source*</span></span> |<span data-ttu-id="07fa5-p101">省略可能です。削除するエンティティ (ファイル、ディレクトリなど) を表す URL を含む文字列型 (**String**) の値を指定します。*Source* を省略するか、または空の文字列を指定した場合、現在 [Record](record-object-ado.md) で表されているエンティティが削除されます。Record がコレクション レコード (ディレクトリなど、[RecordType](recordtype-property-ado.md) が **adCollectionRecord** であるもの) である場合は、すべての子 (サブディレクトリなど) も削除されます。</span><span class="sxs-lookup"><span data-stu-id="07fa5-p101">Optional. A **String** value that contains a URL identifying the entity (for example, the file or directory) to be deleted. If *Source* is omitted or specifies an empty string, the entity represented by the current [Record](record-object-ado.md) is deleted. If the Record is a collection record ([RecordType](recordtype-property-ado.md) of **adCollectionRecord**, such as a directory) all children (for example, subdirectories) will also be deleted.</span></span>|
|<span data-ttu-id="07fa5-115">*Async*</span><span class="sxs-lookup"><span data-stu-id="07fa5-115">*Async*</span></span> |<span data-ttu-id="07fa5-p102">省略可能です。ブール型 ( **Boolean** ) の値を指定します。 **True** のときは、削除操作が非同期で実行されることを示します。</span><span class="sxs-lookup"><span data-stu-id="07fa5-p102">Optional. A **Boolean** value that, when **True**, specifies that the delete operation is asynchronous.</span></span>|

## <a name="remarks"></a><span data-ttu-id="07fa5-118">注釈</span><span class="sxs-lookup"><span data-stu-id="07fa5-118">Remarks</span></span>

<span data-ttu-id="07fa5-p103">このメソッドの終了後、**Record** で表されているオブジェクトに対する操作が失敗する場合があります。**DeleteRecord** を呼び出した後は **Record** を閉じる必要があります。これは、プロバイダーがデータ ソースで **Record** をいつ更新するかにより、**Record** の動作が予期できなくなることがあるためです。</span><span class="sxs-lookup"><span data-stu-id="07fa5-p103">Operations on the object represented by this **Record** may fail after this method completes. After calling **DeleteRecord**, the **Record** should be closed because the behavior of the **Record** may become unpredictable depending upon when the provider updates the **Record** with the data source.</span></span>

<span data-ttu-id="07fa5-121">If this **Record** was obtained from a [Recordset](recordset-object-ado.md), then the results of this operation will not be reflected immediately in the **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="07fa5-121">If this **Record** was obtained from a [Recordset](recordset-object-ado.md), then the results of this operation will not be reflected immediately in the **Recordset**.</span></span> <span data-ttu-id="07fa5-122">recordset を最新の情報に更新するには、**レコードセット**をいったん閉じてから開き直すか、または**recordset**の再[クエリ](requery-method-ado.md)を実行するか、 [Update](update-method-ado.md)メソッドと[Resync](resync-method-ado.md)メソッドを実行します。</span><span class="sxs-lookup"><span data-stu-id="07fa5-122">Refresh the **Recordset** by closing and re-opening it, or by executing the **Recordset** [Requery](requery-method-ado.md), or [Update](update-method-ado.md) and [Resync](resync-method-ado.md) methods.</span></span>

> [!NOTE]
> <span data-ttu-id="07fa5-123">[!メモ] http スキームを使用している URL は、[Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) を自動的に呼び出します。</span><span class="sxs-lookup"><span data-stu-id="07fa5-123">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="07fa5-124">詳細については、「[絶対 url と相対 url](absolute-and-relative-urls.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="07fa5-124">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


