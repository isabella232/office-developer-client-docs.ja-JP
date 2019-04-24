---
title: SourceTable プロパティ (DAO)
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
localization_priority: Normal
ms.openlocfilehash: a557a4941f5b4aa511489c5d057871df5fa72c08
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292987"
---
# <a name="fieldsourcetable-property-dao"></a><span data-ttu-id="7e5b3-102">SourceTable プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="7e5b3-102">Field.SourceTable property (DAO)</span></span>


<span data-ttu-id="7e5b3-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="7e5b3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7e5b3-p101">**Field** オブジェクトの元のデータ ソースとなるテーブルの名前を示す値を取得します。値の取得のみ可能です。文字列型 ( **String**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="7e5b3-p101">Returns a value that indicates the name of the table that is the original source of the data for a **Field** object. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e5b3-106">構文</span><span class="sxs-lookup"><span data-stu-id="7e5b3-106">Syntax</span></span>

<span data-ttu-id="7e5b3-107">*式*。SourceTable</span><span class="sxs-lookup"><span data-stu-id="7e5b3-107">*expression* .SourceTable</span></span>

<span data-ttu-id="7e5b3-108">\*式\***Field**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="7e5b3-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e5b3-109">注釈</span><span class="sxs-lookup"><span data-stu-id="7e5b3-109">Remarks</span></span>

<span data-ttu-id="7e5b3-110">**Field** オブジェクトでは、 **SourceField** プロパティおよび **SourceTable** プロパティの使用方法は、次の表に示すように、 **Field** オブジェクトを追加する **Fields** コレクションが含まれているオブジェクトに応じて異なります。</span><span class="sxs-lookup"><span data-stu-id="7e5b3-110">For a **Field** object, use of the **SourceField** and **SourceTable** properties depends on the object that contains the **Fields** collection that the **Field** object is appended to, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7e5b3-111">オブジェクトの追加先</span><span class="sxs-lookup"><span data-stu-id="7e5b3-111">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="7e5b3-112">使用方法</span><span class="sxs-lookup"><span data-stu-id="7e5b3-112">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7e5b3-113"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="7e5b3-113"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="7e5b3-114">サポートされていません</span><span class="sxs-lookup"><span data-stu-id="7e5b3-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e5b3-115"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="7e5b3-115"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="7e5b3-116">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="7e5b3-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e5b3-117"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="7e5b3-117"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="7e5b3-118">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="7e5b3-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e5b3-119"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="7e5b3-119"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="7e5b3-120">サポートされません。</span><span class="sxs-lookup"><span data-stu-id="7e5b3-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e5b3-121"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="7e5b3-121"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="7e5b3-122">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="7e5b3-122">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7e5b3-p102">これらのプロパティは、 **Field** オブジェクトに関連付けられている元のフィールドおよびテーブルの名前を示します。たとえば、これらのプロパティを使用すると、クエリ フィールドの元のデータ ソースの名前と基になるテーブルのフィールドの名前に関連性がない場合でも、そのデータ ソースを特定できます。</span><span class="sxs-lookup"><span data-stu-id="7e5b3-p102">These properties indicate the original field and table names associated with a **Field** object. For example, you could use these properties to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table.</span></span>


> [!NOTE]
> <span data-ttu-id="7e5b3-125">[!メモ] テーブル タイプの **Recordset** オブジェクトの **Fields** コレクション内にある **Field** オブジェクトで使用すると、 **SourceTable** プロパティは有効なテーブル名を取得しません。</span><span class="sxs-lookup"><span data-stu-id="7e5b3-125">The **SourceTable** property will not return a meaningful table name if used on a **Field** object in the **Fields** collection of a table-type **Recordset** object.</span></span>


