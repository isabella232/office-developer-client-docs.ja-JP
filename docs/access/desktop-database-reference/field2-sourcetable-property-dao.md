---
title: Field2.SourceTable プロパティ (DAO)
TOCTitle: SourceTable Property
ms:assetid: 24d2fdda-d924-d95e-8458-063dd1d36d5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191839(v=office.15)
ms:contentKeyID: 48543768
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: af404f3b741445ef434c4f3266f89aa318e13ad2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477752"
---
# <a name="field2sourcetable-property-dao"></a><span data-ttu-id="6abc0-102">Field2.SourceTable プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="6abc0-102">Field2.SourceTable Property (DAO)</span></span>


<span data-ttu-id="6abc0-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="6abc0-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6abc0-p101">**Field2** オブジェクトのデータの元のソースであるテーブルの名前を示す値を返します。値の取得のみ可能です。文字列型 ( **String**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="6abc0-p101">Returns a value that indicates the name of the table that is the original source of the data for a **Field2** object. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6abc0-106">構文</span><span class="sxs-lookup"><span data-stu-id="6abc0-106">Syntax</span></span>

<span data-ttu-id="6abc0-107">*式*です。SourceTable</span><span class="sxs-lookup"><span data-stu-id="6abc0-107">*expression* .SourceTable</span></span>

<span data-ttu-id="6abc0-108">\*式\***Field2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="6abc0-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6abc0-109">注釈</span><span class="sxs-lookup"><span data-stu-id="6abc0-109">Remarks</span></span>

<span data-ttu-id="6abc0-110">**Field2** オブジェクトでは、 **SourceField** プロパティと **SourceTable** プロパティを使用できるかどうかは、次の表に示すように、 **Field2** オブジェクトが追加される **Fields** コレクションを含むオブジェクトによって決まります。</span><span class="sxs-lookup"><span data-stu-id="6abc0-110">For a **Field2** object, use of the **SourceField** and **SourceTable** properties depends on the object that contains the **Fields** collection that the **Field2** object is appended to, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6abc0-111">オブジェクトの追加先</span><span class="sxs-lookup"><span data-stu-id="6abc0-111">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="6abc0-112">使用例</span><span class="sxs-lookup"><span data-stu-id="6abc0-112">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6abc0-113"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="6abc0-113"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="6abc0-114">サポートされません。</span><span class="sxs-lookup"><span data-stu-id="6abc0-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6abc0-115"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="6abc0-115"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="6abc0-116">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="6abc0-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6abc0-117"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="6abc0-117"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="6abc0-118">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="6abc0-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6abc0-119"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="6abc0-119"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="6abc0-120">サポートされません。</span><span class="sxs-lookup"><span data-stu-id="6abc0-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6abc0-121"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="6abc0-121"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="6abc0-122">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="6abc0-122">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6abc0-p102">これらのプロパティは、 **Field2** オブジェクトに関連付けられた元のフィールドおよびテーブル名を示します。たとえば、これらのプロパティを使用して、基になるテーブルのフィールド名に無関係な名前を持つクエリ フィールド内データの元のソースを調べることができます。</span><span class="sxs-lookup"><span data-stu-id="6abc0-p102">These properties indicate the original field and table names associated with a **Field2** object. For example, you could use these properties to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table.</span></span>


> [!NOTE]
> <P><span data-ttu-id="6abc0-125">[!メモ] <STRONG>SourceTable</STRONG> プロパティは、テーブル タイプの <STRONG>Recordset</STRONG> オブジェクトの <STRONG>Fields</STRONG> コレクションに含まれる <STRONG>Field2</STRONG> オブジェクトで使用した場合、有効なテーブル名を返しません。</span><span class="sxs-lookup"><span data-stu-id="6abc0-125">The <STRONG>SourceTable</STRONG> property will not return a meaningful table name if used on a <STRONG>Field2</STRONG> object in the <STRONG>Fields</STRONG> collection of a table-type <STRONG>Recordset</STRONG> object.</span></span></P>


