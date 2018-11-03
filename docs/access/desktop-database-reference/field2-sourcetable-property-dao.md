---
title: Field2.SourceTable プロパティ (DAO)
TOCTitle: SourceTable Property
ms:assetid: 24d2fdda-d924-d95e-8458-063dd1d36d5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191839(v=office.15)
ms:contentKeyID: 48543768
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 253be078fa6a8f5fdd4cb0c6c67fc6d5385e554c
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936540"
---
# <a name="field2sourcetable-property-dao"></a><span data-ttu-id="3de73-102">Field2.SourceTable プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="3de73-102">Field2.SourceTable property (DAO)</span></span>


<span data-ttu-id="3de73-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="3de73-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3de73-p101">**Field2** オブジェクトのデータの元のソースであるテーブルの名前を示す値を返します。値の取得のみ可能です。文字列型 ( **String**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="3de73-p101">Returns a value that indicates the name of the table that is the original source of the data for a **Field2** object. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="3de73-106">構文</span><span class="sxs-lookup"><span data-stu-id="3de73-106">Syntax</span></span>

<span data-ttu-id="3de73-107">*式*です。SourceTable</span><span class="sxs-lookup"><span data-stu-id="3de73-107">*expression* .SourceTable</span></span>

<span data-ttu-id="3de73-108">\*式\***Field2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="3de73-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3de73-109">注釈</span><span class="sxs-lookup"><span data-stu-id="3de73-109">Remarks</span></span>

<span data-ttu-id="3de73-110">**Field2** オブジェクトでは、 **SourceField** プロパティと **SourceTable** プロパティを使用できるかどうかは、次の表に示すように、 **Field2** オブジェクトが追加される **Fields** コレクションを含むオブジェクトによって決まります。</span><span class="sxs-lookup"><span data-stu-id="3de73-110">For a **Field2** object, use of the **SourceField** and **SourceTable** properties depends on the object that contains the **Fields** collection that the **Field2** object is appended to, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3de73-111">オブジェクトの追加先</span><span class="sxs-lookup"><span data-stu-id="3de73-111">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="3de73-112">使用例</span><span class="sxs-lookup"><span data-stu-id="3de73-112">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3de73-113"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="3de73-113"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="3de73-114">サポートされません。</span><span class="sxs-lookup"><span data-stu-id="3de73-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3de73-115"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="3de73-115"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="3de73-116">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="3de73-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3de73-117"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="3de73-117"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="3de73-118">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="3de73-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3de73-119"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="3de73-119"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="3de73-120">サポートされません。</span><span class="sxs-lookup"><span data-stu-id="3de73-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3de73-121"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="3de73-121"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="3de73-122">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="3de73-122">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3de73-p102">これらのプロパティは、 **Field2** オブジェクトに関連付けられた元のフィールドおよびテーブル名を示します。たとえば、これらのプロパティを使用して、基になるテーブルのフィールド名に無関係な名前を持つクエリ フィールド内データの元のソースを調べることができます。</span><span class="sxs-lookup"><span data-stu-id="3de73-p102">These properties indicate the original field and table names associated with a **Field2** object. For example, you could use these properties to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table.</span></span>


> [!NOTE]
> <span data-ttu-id="3de73-125">[!メモ] **SourceTable** プロパティは、テーブル タイプの **Recordset** オブジェクトの **Fields** コレクションに含まれる **Field2** オブジェクトで使用した場合、有効なテーブル名を返しません。</span><span class="sxs-lookup"><span data-stu-id="3de73-125">The **SourceTable** property will not return a meaningful table name if used on a **Field2** object in the **Fields** collection of a table-type **Recordset** object.</span></span>


