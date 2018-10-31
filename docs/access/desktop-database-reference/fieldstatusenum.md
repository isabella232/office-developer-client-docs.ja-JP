---
title: FieldStatusEnum (デスクトップ データベース参照のアクセス)
TOCTitle: FieldStatusEnum
ms:assetid: 49570042-8435-8618-3ba1-7006c47735e0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249225(v=office.15)
ms:contentKeyID: 48544635
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 22c5d53427d1380273ea82b3a28ae044e103b179
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860610"
---
# <a name="fieldstatusenum"></a><span data-ttu-id="363b4-102">FieldStatusEnum</span><span class="sxs-lookup"><span data-stu-id="363b4-102">FieldStatusEnum</span></span>

<span data-ttu-id="363b4-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="363b4-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="363b4-104">**Field** オブジェクトの状態を表します。</span><span class="sxs-lookup"><span data-stu-id="363b4-104">Specifies the status of a **Field** object.</span></span>

<span data-ttu-id="363b4-105">**adFieldPending\*** 値は、状態を設定する原因となった操作を示し、他の状態値と組み合わせて使用される場合があります。</span><span class="sxs-lookup"><span data-stu-id="363b4-105">The **adFieldPending\*** values indicate the operation that caused the status to be set, and may be combined with other status values.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="363b4-106">定数</span><span class="sxs-lookup"><span data-stu-id="363b4-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="363b4-107">値</span><span class="sxs-lookup"><span data-stu-id="363b4-107">Value</span></span></p></th>
<th><p><span data-ttu-id="363b4-108">説明</span><span class="sxs-lookup"><span data-stu-id="363b4-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="363b4-109"><strong>adFieldAlreadyExists</strong></span><span class="sxs-lookup"><span data-stu-id="363b4-109"><strong>adFieldAlreadyExists</strong></span></span></p></td>
<td><p><span data-ttu-id="363b4-110">26</span><span class="sxs-lookup"><span data-stu-id="363b4-110">26</span></span></p></td>
<td><p><span data-ttu-id="363b4-111">指定したフィールドが既に存在することを示します。</span><span class="sxs-lookup"><span data-stu-id="363b4-111">Indicates that the specified field already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="363b4-112"><strong>adFieldBadStatus</strong></span><span class="sxs-lookup"><span data-stu-id="363b4-112"><strong>adFieldBadStatus</strong></span></span></p></td>
<td><p><span data-ttu-id="363b4-113">12</span><span class="sxs-lookup"><span data-stu-id="363b4-113">12</span></span></p></td>
<td><p><span data-ttu-id="363b4-p101">ADO から OLE DB プロバイダーに無効な状態値が送信されたことを示します。原因としては、OLE DB 1.0 プロバイダーまたは 1.1 プロバイダー、あるいは不適切な組み合わせの <a href="value-property-ado.md">Value</a> と <a href="status-property-ado-field.md">Status</a> が考えられます。</span><span class="sxs-lookup"><span data-stu-id="363b4-p101">Indicates that an invalid status value was sent from ADO to the OLE DB provider. Possible causes include an OLE DB 1.0 or 1.1 provider, or an improper combination of <a href="value-property-ado.md">Value</a> and <a href="status-property-ado-field.md">Status</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="363b4-116"><strong>adFieldCannotComplete</strong></span><span class="sxs-lookup"><span data-stu-id="363b4-116"><strong>adFieldCannotComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="363b4-117">20</span><span class="sxs-lookup"><span data-stu-id="363b4-117">20</span></span></p></td>
<td><p><span data-ttu-id="363b4-118"><a href="source-property-ado-record.md">Source</a> で指定された URL のサーバーが操作を完了できなかったことを示します。</span><span class="sxs-lookup"><span data-stu-id="363b4-118">Indicates that the server of the URL specified by <a href="source-property-ado-record.md">Source</a> could not complete the operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="363b4-119"><strong>adFieldCannotDeleteSource</strong></span><span class="sxs-lookup"><span data-stu-id="363b4-119"><strong>adFieldCannotDeleteSource</strong></span></span></p></td>
<td><p><span data-ttu-id="363b4-120">23</span><span class="sxs-lookup"><span data-stu-id="363b4-120">23</span></span></p></td>
<td><p><span data-ttu-id="363b4-121">移動操作で、ツリーまたはサブツリーを新しい位置に移動したがソースを削除できなかったことを示します。</span><span class="sxs-lookup"><span data-stu-id="363b4-121">Indicates that during a move operation, a tree or subtree was moved to a new location, but the source could not be deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="363b4-122"><strong>adFieldCantConvertValue</strong></span><span class="sxs-lookup"><span data-stu-id="363b4-122"><strong>adFieldCantConvertValue</strong></span></span></p></td>
<td><p><span data-ttu-id="363b4-123">2</span><span class="sxs-lookup"><span data-stu-id="363b4-123">2</span></span></p></td>
<td><p><span data-ttu-id="363b4-124">フィールドの取得または保存を行うときにデータが失われてしまうことを示します。</span><span class="sxs-lookup"><span data-stu-id="363b4-124">Indicates that the field cannot be retrieved or stored without loss of data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="363b4-125"><strong>adFieldCantCreate</strong></span><span class="sxs-lookup"><span data-stu-id="363b4-125"><strong>adFieldCantCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="363b4-126">7</span><span class="sxs-lookup"><span data-stu-id="363b4-126">7</span></span></p></td>
<td><p><span data-ttu-id="363b4-127">プロバイダーの限度 (許容フィールド数など) を超えたためにフィールドを追加できなかったことを示します。</span><span class="sxs-lookup"><span data-stu-id="363b4-127">Indicates that the field could not be added because the provider exceeded a limitation (such as the number of fields allowed).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="363b4-128"><strong>adFieldDataOverflow</strong></span><span class="sxs-lookup"><span data-stu-id="363b4-128"><strong>adFieldDataOverflow</strong></span></span></p></td>
<td><p><span data-ttu-id="363b4-129">6</span><span class="sxs-lookup"><span data-stu-id="363b4-129">6</span></span></p></td>
<td><p><span data-ttu-id="363b4-130">プロバイダーから返されたデータがフィールドのデータ型をオーバーフローしたことを示します。</span><span class="sxs-lookup"><span data-stu-id="363b4-130">Indicates that the data returned from the provider overflowed the data type of the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="363b4-131"><strong>adFieldDefault</strong></span><span class="sxs-lookup"><span data-stu-id="363b4-131"><strong>adFieldDefault</strong></span></span></p></td>
<td><p><span data-ttu-id="363b4-132">13</span><span class="sxs-lookup"><span data-stu-id="363b4-132">13</span></span></p></td>
<td><p><span data-ttu-id="363b4-133">データの設定時にフィールドの既定値が使われたことを示します。</span><span class="sxs-lookup"><span data-stu-id="363b4-133">Indicates that the default value for the field was used when setting data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="363b4-134"><strong>adFieldDoesNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="363b4-134"><strong>adFieldDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="363b4-135">16</span><span class="sxs-lookup"><span data-stu-id="363b4-135">16</span></span></p></td>
<td><p><span data-ttu-id="363b4-136">指定したフィールドが存在しないことを示します。</span><span class="sxs-lookup"><span data-stu-id="363b4-136">Indicates that the field specified does not exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="363b4-137"><strong>adFieldIgnore</strong></span><span class="sxs-lookup"><span data-stu-id="363b4-137"><strong>adFieldIgnore</strong></span></span></p></td>
<td><p><span data-ttu-id="363b4-138">15</span><span class="sxs-lookup"><span data-stu-id="363b4-138">15</span></span></p></td>
<td><p><span data-ttu-id="363b4-p102">ソースでのデータ値の設定時にこのフィールドがスキップされたことを示します。プロバイダーで値が設定されませんでした。</span><span class="sxs-lookup"><span data-stu-id="363b4-p102">Indicates that this field was skipped when setting data values in the source. The provider set no value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="363b4-141"><strong>adFieldIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="363b4-141"><strong>adFieldIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="363b4-142">10</span><span class="sxs-lookup"><span data-stu-id="363b4-142">10</span></span></p></td>
<td><p><span data-ttu-id="363b4-143">計算エンティティまたは派生エンティティであるため、フィールドを編集できないことを示します。</span><span class="sxs-lookup"><span data-stu-id="363b4-143">Indicates that the field cannot be modified because it is a calculated or derived entity.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="363b4-144"><strong>adFieldInvalidURL</strong></span><span class="sxs-lookup"><span data-stu-id="363b4-144"><strong>adFieldInvalidURL</strong></span></span></p></td>
<td><p><span data-ttu-id="363b4-145">17</span><span class="sxs-lookup"><span data-stu-id="363b4-145">17</span></span></p></td>
<td><p><span data-ttu-id="363b4-146">データ ソース URL に無効な文字があることを示します。</span><span class="sxs-lookup"><span data-stu-id="363b4-146">Indicates that the data source URL contains invalid characters.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="363b4-147"><strong>adFieldIsNull</strong></span><span class="sxs-lookup"><span data-stu-id="363b4-147"><strong>adFieldIsNull</strong></span></span></p></td>
<td><p><span data-ttu-id="363b4-148">3</span><span class="sxs-lookup"><span data-stu-id="363b4-148">3</span></span></p></td>
<td><p><span data-ttu-id="363b4-149">プロバイダーが種類 VT_NULL のバリアント型 (VARIANT) の値を返し、フィールドが空でないことを示します。</span><span class="sxs-lookup"><span data-stu-id="363b4-149">Indicates that the provider returned a VARIANT value of type VT_NULL and that the field is not empty.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="363b4-150"><strong>adfieldok で</strong></span><span class="sxs-lookup"><span data-stu-id="363b4-150"><strong>adFieldOK</strong></span></span></p></td>
<td><p><span data-ttu-id="363b4-151">0</span><span class="sxs-lookup"><span data-stu-id="363b4-151">0</span></span></p></td>
<td><p><span data-ttu-id="363b4-p103">既定値。フィールドの追加または削除が正常に行われたことを示します。</span><span class="sxs-lookup"><span data-stu-id="363b4-p103">Default. Indicates that the field was successfully added or deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="363b4-154"><strong>adFieldOutOfSpace</strong></span><span class="sxs-lookup"><span data-stu-id="363b4-154"><strong>adFieldOutOfSpace</strong></span></span></p></td>
<td><p><span data-ttu-id="363b4-155">22</span><span class="sxs-lookup"><span data-stu-id="363b4-155">22</span></span></p></td>
<td><p><span data-ttu-id="363b4-156">移動またはコピー操作を実行するために必要な記憶域をプロバイダーが確保できないことを示します。</span><span class="sxs-lookup"><span data-stu-id="363b4-156">Indicates that the provider is unable to obtain enough storage space to complete a move or copy operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="363b4-157"><strong>adFieldPendingChange</strong></span><span class="sxs-lookup"><span data-stu-id="363b4-157"><strong>adFieldPendingChange</strong></span></span></p></td>
<td><p><span data-ttu-id="363b4-158">0x40000</span><span class="sxs-lookup"><span data-stu-id="363b4-158">0x40000</span></span></p></td>
<td><p><span data-ttu-id="363b4-p104">フィールドが削除され、異なるデータ型を指定して再度追加されたか、以前に状態が adFieldOK であったフィールドの値が変更されたことを示します。<a href="update-method-ado.md">Update</a> メソッドの呼び出し後にフィールドの最終形式によって <a href="fields-collection-ado.md">Fields</a> コレクションが変更されます。</span><span class="sxs-lookup"><span data-stu-id="363b4-p104">Indicates either that the field has been deleted and then re-added, perhaps with a different data type, or that the value of the field that previously had a status of adFieldOK has changed. The final form of the field will modify the <a href="fields-collection-ado.md">Fields</a> collection after the <a href="update-method-ado.md">Update</a> method is called.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="363b4-161"><strong>adFieldPendingDelete</strong></span><span class="sxs-lookup"><span data-stu-id="363b4-161"><strong>adFieldPendingDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="363b4-162">0x20000</span><span class="sxs-lookup"><span data-stu-id="363b4-162">0x20000</span></span></p></td>
<td><p><span data-ttu-id="363b4-p105"><strong>Delete</strong> 操作で状態が設定されたことを示します。フィールドは、<strong>Update</strong> メソッドの呼び出し後に <strong>Fields</strong> コレクションから削除するようマークされています。</span><span class="sxs-lookup"><span data-stu-id="363b4-p105">Indicates that the <strong>Delete</strong> operation caused the status to be set. The field has been marked for deletion from the <strong>Fields</strong> collection after the <strong>Update</strong> method is called.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="363b4-165"><strong>adFieldPendingInsert</strong></span><span class="sxs-lookup"><span data-stu-id="363b4-165"><strong>adFieldPendingInsert</strong></span></span></p></td>
<td><p><span data-ttu-id="363b4-166">0x10000</span><span class="sxs-lookup"><span data-stu-id="363b4-166">0x10000</span></span></p></td>
<td><p><span data-ttu-id="363b4-p106"><strong>Append</strong> 操作で状態が設定されたことを示します。<strong>Field</strong> は、<strong>Update</strong> メソッドの呼び出し後に <strong>Fields</strong> コレクションに追加するようマークされています。</span><span class="sxs-lookup"><span data-stu-id="363b4-p106">Indicates that the <strong>Append</strong> operation caused the status to be set. The <strong>Field</strong> has been marked to be added to the <strong>Fields</strong> collection after the <strong>Update</strong> method is called.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="363b4-169"><strong>adFieldPendingUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="363b4-169"><strong>adFieldPendingUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="363b4-170">これに対して、0x80000</span><span class="sxs-lookup"><span data-stu-id="363b4-170">0x80000</span></span></p></td>
<td><p><span data-ttu-id="363b4-171">フィールドの状態を設定する原因となった操作をプロバイダーが判別できないことを示します。</span><span class="sxs-lookup"><span data-stu-id="363b4-171">Indicates that the provider cannot determine what operation caused field status to be set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="363b4-172"><strong>adFieldPendingUnknownDelete</strong></span><span class="sxs-lookup"><span data-stu-id="363b4-172"><strong>adFieldPendingUnknownDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="363b4-173">0x100000</span><span class="sxs-lookup"><span data-stu-id="363b4-173">0x100000</span></span></p></td>
<td><p><span data-ttu-id="363b4-174">フィールドの状態を設定する原因となった操作をプロバイダーが判別できず、<strong>Update</strong> メソッドの呼び出し後に <strong>Fields</strong> コレクションからフィールドが削除されることを示します。</span><span class="sxs-lookup"><span data-stu-id="363b4-174">Indicates that the provider cannot determine what operation caused field status to be set, and that the field will be deleted from the <strong>Fields</strong> collection after the <strong>Update</strong> method is called.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="363b4-175"><strong>adFieldPermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="363b4-175"><strong>adFieldPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="363b4-176">9</span><span class="sxs-lookup"><span data-stu-id="363b4-176">9</span></span></p></td>
<td><p><span data-ttu-id="363b4-177">読み取り専用として定義されているため、フィールドを編集できないことを示します。</span><span class="sxs-lookup"><span data-stu-id="363b4-177">Indicates that the field cannot be modified because it is defined as read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="363b4-178"><strong>adFieldReadOnly</strong></span><span class="sxs-lookup"><span data-stu-id="363b4-178"><strong>adFieldReadOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="363b4-179">24</span><span class="sxs-lookup"><span data-stu-id="363b4-179">24</span></span></p></td>
<td><p><span data-ttu-id="363b4-180">データ ソース内のフィールドが読み取り専用として定義されていることを示します。</span><span class="sxs-lookup"><span data-stu-id="363b4-180">Indicates that the field in the data source is defined as read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="363b4-181"><strong>adFieldResourceExists</strong></span><span class="sxs-lookup"><span data-stu-id="363b4-181"><strong>adFieldResourceExists</strong></span></span></p></td>
<td><p><span data-ttu-id="363b4-182">19</span><span class="sxs-lookup"><span data-stu-id="363b4-182">19</span></span></p></td>
<td><p><span data-ttu-id="363b4-183">宛先 URL にオブジェクトが既に存在し、上書きできないため、プロバイダーが操作を実行できなかったことを示します。</span><span class="sxs-lookup"><span data-stu-id="363b4-183">Indicates that the provider was unable to perform the operation because an object already exists at the destination URL and it is not able to overwrite the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="363b4-184"><strong>adFieldResourceLocked</strong></span><span class="sxs-lookup"><span data-stu-id="363b4-184"><strong>adFieldResourceLocked</strong></span></span></p></td>
<td><p><span data-ttu-id="363b4-185">18</span><span class="sxs-lookup"><span data-stu-id="363b4-185">18</span></span></p></td>
<td><p><span data-ttu-id="363b4-186">データ ソースが 1 つ以上の他のアプリケーションまたはプロセスによってロックされているため、プロバイダーが操作を実行できなかったことを示します。</span><span class="sxs-lookup"><span data-stu-id="363b4-186">Indicates that the provider was unable to perform the operation because the data source is locked by one or more other application or process.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="363b4-187"><strong>adFieldResourceOutOfScope</strong></span><span class="sxs-lookup"><span data-stu-id="363b4-187"><strong>adFieldResourceOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="363b4-188">25</span><span class="sxs-lookup"><span data-stu-id="363b4-188">25</span></span></p></td>
<td><p><span data-ttu-id="363b4-189">ソースまたは宛先の URL が現在のレコードの範囲外であることを示します。</span><span class="sxs-lookup"><span data-stu-id="363b4-189">Indicates that a source or destination URL is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="363b4-190"><strong>adFieldSchemaViolation</strong></span><span class="sxs-lookup"><span data-stu-id="363b4-190"><strong>adFieldSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="363b4-191">11</span><span class="sxs-lookup"><span data-stu-id="363b4-191">11</span></span></p></td>
<td><p><span data-ttu-id="363b4-192">値がフィールドのデータ ソース スキーマ制約に違反することを示します。</span><span class="sxs-lookup"><span data-stu-id="363b4-192">Indicates that the value violated the data source schema constraint for the field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="363b4-193"><strong>adFieldSignMismatch</strong></span><span class="sxs-lookup"><span data-stu-id="363b4-193"><strong>adFieldSignMismatch</strong></span></span></p></td>
<td><p><span data-ttu-id="363b4-194">5</span><span class="sxs-lookup"><span data-stu-id="363b4-194">5</span></span></p></td>
<td><p><span data-ttu-id="363b4-195">プロバイダーが返すデータ値が符号付きで、ADO フィールド値のデータ型が符号なしであることを示します。</span><span class="sxs-lookup"><span data-stu-id="363b4-195">Indicates that data value returned by the provider was signed but the data type of the ADO field value was unsigned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="363b4-196"><strong>adFieldTruncated</strong></span><span class="sxs-lookup"><span data-stu-id="363b4-196"><strong>adFieldTruncated</strong></span></span></p></td>
<td><p><span data-ttu-id="363b4-197">4</span><span class="sxs-lookup"><span data-stu-id="363b4-197">4</span></span></p></td>
<td><p><span data-ttu-id="363b4-198">データ ソースからの読み取り時に可変長データが切り捨てられたことを示します。</span><span class="sxs-lookup"><span data-stu-id="363b4-198">Indicates that variable-length data was truncated when reading from the data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="363b4-199"><strong>adFieldUnavailable</strong></span><span class="sxs-lookup"><span data-stu-id="363b4-199"><strong>adFieldUnavailable</strong></span></span></p></td>
<td><p><span data-ttu-id="363b4-200">8</span><span class="sxs-lookup"><span data-stu-id="363b4-200">8</span></span></p></td>
<td><p><span data-ttu-id="363b4-p107">データ ソースからの読み取り時にプロバイダーが値を判別できなかったことを示します。たとえば、行が作成された直後であること、列の既定値が使用不可であること、または新しい値がまだ指定されていないことが原因として考えられます。</span><span class="sxs-lookup"><span data-stu-id="363b4-p107">Indicates that the provider could not determine the value when reading from the data source. For example, the row was just created, the default value for the column was not available, and a new value had not yet been specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="363b4-203"><strong>adFieldVolumeNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="363b4-203"><strong>adFieldVolumeNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="363b4-204">21</span><span class="sxs-lookup"><span data-stu-id="363b4-204">21</span></span></p></td>
<td><p><span data-ttu-id="363b4-205">URL が示す記憶域ボリュームをプロバイダーが特定できないことを示します。</span><span class="sxs-lookup"><span data-stu-id="363b4-205">Indicates that the provider is unable to locate the storage volume indicated by the URL.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="363b4-206">ADO/WFC に相当</span><span class="sxs-lookup"><span data-stu-id="363b4-206">ADO/WFC equivalent</span></span>

<span data-ttu-id="363b4-207">これらの定数に ADO/WFC 等価はありません。</span><span class="sxs-lookup"><span data-stu-id="363b4-207">These constants do not have ADO/WFC equivalents.</span></span>

