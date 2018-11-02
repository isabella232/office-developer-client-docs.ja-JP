---
title: Field2.SourceField プロパティ (DAO)
TOCTitle: SourceField Property
ms:assetid: f89146c1-d4a4-1129-636a-c22cf7921a4e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836948(v=office.15)
ms:contentKeyID: 48548784
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 587214a5fddc5774423d2eb5af7c2a8926ee1622
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926270"
---
# <a name="field2sourcefield-property-dao"></a><span data-ttu-id="d8f2f-102">Field2.SourceField プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="d8f2f-102">Field2.SourceField property (DAO)</span></span>


<span data-ttu-id="d8f2f-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="d8f2f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d8f2f-p101">**Field2** オブジェクトのデータの元のソースであるフィールドの名前を示す値を返します。値の取得のみ可能です。文字列型 ( **String**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="d8f2f-p101">Returns a value that indicates the name of the field that is the original source of the data for a **Field2** object. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8f2f-106">構文</span><span class="sxs-lookup"><span data-stu-id="d8f2f-106">Syntax</span></span>

<span data-ttu-id="d8f2f-107">*式*です。SourceField</span><span class="sxs-lookup"><span data-stu-id="d8f2f-107">*expression* .SourceField</span></span>

<span data-ttu-id="d8f2f-108">\*式\***Field2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="d8f2f-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8f2f-109">注釈</span><span class="sxs-lookup"><span data-stu-id="d8f2f-109">Remarks</span></span>

<span data-ttu-id="d8f2f-110">**Field2** オブジェクトでは、 **SourceField** プロパティと **SourceTable** プロパティを使用できるかどうかは、次の表に示すように、 **Field2** オブジェクトが追加される **Fields** コレクションを含むオブジェクトによって決まります。</span><span class="sxs-lookup"><span data-stu-id="d8f2f-110">For a **Field2** object, use of the **SourceField** and **SourceTable** properties depends on the object that contains the **Fields** collection that the **Field2** object is appended to, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d8f2f-111">オブジェクトの追加先</span><span class="sxs-lookup"><span data-stu-id="d8f2f-111">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="d8f2f-112">使用例</span><span class="sxs-lookup"><span data-stu-id="d8f2f-112">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d8f2f-113"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="d8f2f-113"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="d8f2f-114">サポートされません。</span><span class="sxs-lookup"><span data-stu-id="d8f2f-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8f2f-115"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="d8f2f-115"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="d8f2f-116">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="d8f2f-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8f2f-117"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="d8f2f-117"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="d8f2f-118">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="d8f2f-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8f2f-119"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="d8f2f-119"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="d8f2f-120">サポートされません。</span><span class="sxs-lookup"><span data-stu-id="d8f2f-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8f2f-121"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="d8f2f-121"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="d8f2f-122">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="d8f2f-122">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d8f2f-p102">これらのプロパティは、 **Field2** オブジェクトに関連付けられた元のフィールドおよびテーブル名を示します。たとえば、これらのプロパティを使用して、クエリ フィールド内の、基になるテーブルのフィールド名に無関係な名前を持つデータの、元のソースを調べることができます。</span><span class="sxs-lookup"><span data-stu-id="d8f2f-p102">These properties indicate the original field and table names associated with a **Field2** object. For example, you could use these properties to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table.</span></span>

