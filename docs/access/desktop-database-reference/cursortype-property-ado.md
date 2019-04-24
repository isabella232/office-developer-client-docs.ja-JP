---
title: CursorType プロパティ (ADO)
TOCTitle: CursorType property (ADO)
ms:assetid: f42ded8f-9f92-ef03-a198-ffb892324611
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250239(v=office.15)
ms:contentKeyID: 48548682
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7cdb32bb8ff9bb6e0556a87de0efe82cd919dbe2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295185"
---
# <a name="cursortype-property-ado"></a><span data-ttu-id="3cc67-102">CursorType プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="3cc67-102">CursorType property (ADO)</span></span>


<span data-ttu-id="3cc67-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="3cc67-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3cc67-104">[Recordset](recordset-object-ado.md) オブジェクトで使用されているカーソルの種類を示します。</span><span class="sxs-lookup"><span data-stu-id="3cc67-104">Indicates the type of cursor used in a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="3cc67-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="3cc67-105">Settings and return values</span></span>

<span data-ttu-id="3cc67-106">[CursorTypeEnum](cursortypeenum.md) の値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="3cc67-106">Sets or returns a [CursorTypeEnum](cursortypeenum.md) value.</span></span> <span data-ttu-id="3cc67-107">既定値は **adOpenForwardOnly** です。</span><span class="sxs-lookup"><span data-stu-id="3cc67-107">The default value is **adOpenForwardOnly**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3cc67-108">注釈</span><span class="sxs-lookup"><span data-stu-id="3cc67-108">Remarks</span></span>

<span data-ttu-id="3cc67-109">**CursorType** プロパティでは、**Recordset** オブジェクトを開くときに使うカーソルの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="3cc67-109">Use the **CursorType** property to specify the type of cursor that should be used when opening the **Recordset** object.</span></span>

<span data-ttu-id="3cc67-p102">**CursorLocation** プロパティが [adUseClient](cursorlocation-property-ado.md) に設定されている場合は、 **adOpenStatic** の設定だけがサポートされます。サポートされていない値が設定された場合でも、エラーは発生しません。サポートされている **CursorType** のうち、一番近い値で代用されます。</span><span class="sxs-lookup"><span data-stu-id="3cc67-p102">Only a setting of **adOpenStatic** is supported if the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**. If an unsupported value is set, then no error will result; the closest supported **CursorType** will be used instead.</span></span>

<span data-ttu-id="3cc67-p103">要求されたカーソルの種類をサポートしていない場合、プロバイダーは他のカーソルの種類を返します。**Recordset** オブジェクトが開いているときには、 [CursorType](recordset-object-ado.md) プロパティは実際に使用されているカーソルの種類に合わせて変更されます。返されたカーソル特有の機能を調べるには、 [Supports](supports-method-ado.md) メソッドを使用します。 **Recordset** を閉じると、 **CursorType** プロパティは元の設定値に戻ります。</span><span class="sxs-lookup"><span data-stu-id="3cc67-p103">If a provider does not support the requested cursor type, it may return another cursor type. The **CursorType** property will change to match the actual cursor type in use when the [Recordset](recordset-object-ado.md) object is open. To verify specific functionality of the returned cursor, use the [Supports](supports-method-ado.md) method. After you close the **Recordset**, the **CursorType** property reverts to its original setting.</span></span>

<span data-ttu-id="3cc67-116">次の表では、各カーソルの種類に必要なプロバイダーの機能 ( **Supports** メソッドの定数によって識別されます) を示します。</span><span class="sxs-lookup"><span data-stu-id="3cc67-116">The following chart shows the provider functionality (identified by **Supports** method constants) required for each cursor type.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3cc67-117">Recordset の CursorType</span><span class="sxs-lookup"><span data-stu-id="3cc67-117">For a Recordset of this CursorType</span></span></p></th>
<th><p><span data-ttu-id="3cc67-118">Supports メソッドが True を返す定数</span><span class="sxs-lookup"><span data-stu-id="3cc67-118">The Supports method must return True for all of these constants</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3cc67-119"><strong>adOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="3cc67-119"><strong>adOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="3cc67-120">none</span><span class="sxs-lookup"><span data-stu-id="3cc67-120">none</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cc67-121"><strong>adopenkeyset</strong></span><span class="sxs-lookup"><span data-stu-id="3cc67-121"><strong>adOpenKeyset</strong></span></span></p></td>
<td><p><span data-ttu-id="3cc67-122"><strong>adbookmark</strong>、 <strong>adHoldRecords</strong>、 <strong>adMovePrevious</strong>、 <strong>adbookmark</strong></span><span class="sxs-lookup"><span data-stu-id="3cc67-122"><strong>adBookmark</strong>, <strong>adHoldRecords</strong>, <strong>adMovePrevious</strong>, <strong>adResync</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cc67-123"><strong>adOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="3cc67-123"><strong>adOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="3cc67-124"><strong>adMovePrevious</strong></span><span class="sxs-lookup"><span data-stu-id="3cc67-124"><strong>adMovePrevious</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cc67-125"><strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="3cc67-125"><strong>adOpenStatic</strong></span></span></p></td>
<td><p><span data-ttu-id="3cc67-126"><strong>adbookmark</strong>、 <strong>adHoldRecords</strong>、 <strong>adMovePrevious</strong>、 <strong>adbookmark</strong></span><span class="sxs-lookup"><span data-stu-id="3cc67-126"><strong>adBookmark</strong>, <strong>adHoldRecords</strong>, <strong>adMovePrevious</strong>, <strong>adResync</strong></span></span></p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> <span data-ttu-id="3cc67-p104">動的カーソルまたは前方のみカーソルで **Supports**(**adUpdateBatch**) が True を返すことがありますが、一括更新ではキーセット カーソルまたは静的カーソルを使用する必要があります。一括更新に必要な Cursor Service for OLE DB を有効にするには、[LockType](locktype-property-ado.md) プロパティを **adLockBatchOptimistic** に設定し、**CursorLocation** プロパティを **adUseClient** に設定します。</span><span class="sxs-lookup"><span data-stu-id="3cc67-p104">Although **Supports**(**adUpdateBatch**) may be true for dynamic and forward-only cursors, for batch updates you should use either a keyset or static cursor. Set the [LockType](locktype-property-ado.md) property to **adLockBatchOptimistic** and the **CursorLocation** property to **adUseClient** to enable the Cursor Service for OLE DB, which is required for batch updates.</span></span>

<span data-ttu-id="3cc67-129">**CursorType** プロパティは、 **Recordset** が閉じているときは読み取り/書き込み可能で、開いているときは読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="3cc67-129">The **CursorType** property is read/write when the **Recordset** is closed and read-only when it is open.</span></span>

<span data-ttu-id="3cc67-130">**リモートデータサービスの使用状況**クライアント側の Recordset オブジェクトで使用する場合、 **CursorType**プロパティは**adopenstatic**にのみ設定できます。</span><span class="sxs-lookup"><span data-stu-id="3cc67-130">**Remote Data Service Usage**When used on a client-side Recordset object, the **CursorType** property can be set only to **adOpenStatic**.</span></span>

