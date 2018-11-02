---
title: Field.SourceTable プロパティ (DAO)
TOCTitle: SourceTable Property
ms:assetid: 9564ea1c-eafd-0b72-fd68-d88fcc3ea189
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197694(v=office.15)
ms:contentKeyID: 48546429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052900
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6bd096b8989cefe48df882d447aab0d4f3d0a6ee
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925199"
---
# <a name="fieldsourcetable-property-dao"></a><span data-ttu-id="e22ea-102">Field.SourceTable プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="e22ea-102">Field.SourceTable property (DAO)</span></span>


<span data-ttu-id="e22ea-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="e22ea-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e22ea-p101">**Field** オブジェクトの元のデータ ソースとなるテーブルの名前を示す値を取得します。値の取得のみ可能です。文字列型 ( **String**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="e22ea-p101">Returns a value that indicates the name of the table that is the original source of the data for a **Field** object. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e22ea-106">構文</span><span class="sxs-lookup"><span data-stu-id="e22ea-106">Syntax</span></span>

<span data-ttu-id="e22ea-107">*式*です。SourceTable</span><span class="sxs-lookup"><span data-stu-id="e22ea-107">*expression* .SourceTable</span></span>

<span data-ttu-id="e22ea-108">\*式\***Field**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="e22ea-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e22ea-109">注釈</span><span class="sxs-lookup"><span data-stu-id="e22ea-109">Remarks</span></span>

<span data-ttu-id="e22ea-110">**Field** オブジェクトでは、 **SourceField** プロパティおよび **SourceTable** プロパティの使用方法は、次の表に示すように、 **Field** オブジェクトを追加する **Fields** コレクションが含まれているオブジェクトに応じて異なります。</span><span class="sxs-lookup"><span data-stu-id="e22ea-110">For a **Field** object, use of the **SourceField** and **SourceTable** properties depends on the object that contains the **Fields** collection that the **Field** object is appended to, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e22ea-111">オブジェクトの追加先</span><span class="sxs-lookup"><span data-stu-id="e22ea-111">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="e22ea-112">使用例</span><span class="sxs-lookup"><span data-stu-id="e22ea-112">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e22ea-113"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="e22ea-113"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="e22ea-114">サポートされません。</span><span class="sxs-lookup"><span data-stu-id="e22ea-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e22ea-115"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="e22ea-115"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="e22ea-116">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="e22ea-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e22ea-117"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="e22ea-117"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="e22ea-118">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="e22ea-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e22ea-119"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="e22ea-119"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="e22ea-120">サポートされません。</span><span class="sxs-lookup"><span data-stu-id="e22ea-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e22ea-121"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="e22ea-121"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="e22ea-122">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="e22ea-122">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e22ea-p102">これらのプロパティは、 **Field** オブジェクトに関連付けられている元のフィールドおよびテーブルの名前を示します。たとえば、これらのプロパティを使用すると、クエリ フィールドの元のデータ ソースの名前と基になるテーブルのフィールドの名前に関連性がない場合でも、そのデータ ソースを特定できます。</span><span class="sxs-lookup"><span data-stu-id="e22ea-p102">These properties indicate the original field and table names associated with a **Field** object. For example, you could use these properties to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table.</span></span>


> [!NOTE]
> <P><span data-ttu-id="e22ea-125">[!メモ] テーブル タイプの <STRONG>Recordset</STRONG> オブジェクトの <STRONG>Fields</STRONG> コレクション内にある <STRONG>Field</STRONG> オブジェクトで使用すると、 <STRONG>SourceTable</STRONG> プロパティは有効なテーブル名を取得しません。</span><span class="sxs-lookup"><span data-stu-id="e22ea-125">The <STRONG>SourceTable</STRONG> property will not return a meaningful table name if used on a <STRONG>Field</STRONG> object in the <STRONG>Fields</STRONG> collection of a table-type <STRONG>Recordset</STRONG> object.</span></span></P>


