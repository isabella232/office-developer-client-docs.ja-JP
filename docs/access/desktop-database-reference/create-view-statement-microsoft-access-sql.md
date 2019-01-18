---
title: CREATE VIEW ステートメント (Microsoft Access SQL)
TOCTitle: CREATE VIEW statement (Microsoft Access SQL)
ms:assetid: ecaabd75-3081-fd35-830d-5a59b0a51922
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836312(v=office.15)
ms:contentKeyID: 48548519
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 73fac5ff9dd1f5cf277b8cb241044af23609b764
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706626"
---
# <a name="create-view-statement-microsoft-access-sql"></a><span data-ttu-id="9b5cd-102">CREATE VIEW ステートメント (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="9b5cd-102">CREATE VIEW statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="9b5cd-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="9b5cd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9b5cd-104">新しいビューを作成します。</span><span class="sxs-lookup"><span data-stu-id="9b5cd-104">Creates a new view.</span></span>

> [!NOTE]
> <span data-ttu-id="9b5cd-105">[!メモ] Microsoft Access データベース エンジンは、Microsoft Access データベース エンジン以外のデータベースでは CREATE VIEW 句や DDL (データ定義言語) ステートメントを使用できません。</span><span class="sxs-lookup"><span data-stu-id="9b5cd-105">The Microsoft Access database engine does not support the use of CREATE VIEW, or any of the DDL statements, with non-Microsoft Access database engine databases.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b5cd-106">構文</span><span class="sxs-lookup"><span data-stu-id="9b5cd-106">Syntax</span></span>

<span data-ttu-id="9b5cd-107">*ビュー*のビューの作成\[(*フィールド 1*\[、*フィールド 2*\[、.\] \])\]として*使いましょう*</span><span class="sxs-lookup"><span data-stu-id="9b5cd-107">CREATE VIEW *view* \[(*field1*\[, *field2*\[, …\]\])\] AS *selectstatement*</span></span>

<span data-ttu-id="9b5cd-108">CREATE VIEW ステートメントには次の指定項目があります。</span><span class="sxs-lookup"><span data-stu-id="9b5cd-108">The CREATE VIEW statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9b5cd-109">指定項目</span><span class="sxs-lookup"><span data-stu-id="9b5cd-109">Part</span></span></p></th>
<th><p><span data-ttu-id="9b5cd-110">説明</span><span class="sxs-lookup"><span data-stu-id="9b5cd-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9b5cd-111"><em>view</em></span><span class="sxs-lookup"><span data-stu-id="9b5cd-111"><em>view</em></span></span></p></td>
<td><p><span data-ttu-id="9b5cd-112">作成するビューの名前。</span><span class="sxs-lookup"><span data-stu-id="9b5cd-112">The name of the view to be created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b5cd-113"><em>field1</em>, <em>field2</em></span><span class="sxs-lookup"><span data-stu-id="9b5cd-113"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="9b5cd-114"><em>selectstatement</em> で指定された関連フィールドのフィールド名。</span><span class="sxs-lookup"><span data-stu-id="9b5cd-114">The name of field or fields for the corresponding fields specified in <em>selectstatement</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b5cd-115"><em>selectstatement</em></span><span class="sxs-lookup"><span data-stu-id="9b5cd-115"><em>selectstatement</em></span></span></p></td>
<td><p><span data-ttu-id="9b5cd-116">SQL SELECT ステートメント。</span><span class="sxs-lookup"><span data-stu-id="9b5cd-116">A SQL SELECT statement.</span></span> <span data-ttu-id="9b5cd-117">詳細については、 <a href="select-statement-microsoft-access-sql.md">SELECT ステートメントを</a>参照してください。</span><span class="sxs-lookup"><span data-stu-id="9b5cd-117">For more information, see <a href="select-statement-microsoft-access-sql.md">SELECT statement</a>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="9b5cd-118">解説</span><span class="sxs-lookup"><span data-stu-id="9b5cd-118">Remarks</span></span>

<span data-ttu-id="9b5cd-119">ビューを定義するのは SELECT ステートメントであり、[SELECT...INTO](select-into-statement-microsoft-access-sql.md) ステートメントではありません。</span><span class="sxs-lookup"><span data-stu-id="9b5cd-119">The SELECT statement that defines the view cannot be a [SELECT INTO](select-into-statement-microsoft-access-sql.md) statement.</span></span>

<span data-ttu-id="9b5cd-120">ビューを定義する SELECT ステートメントは、パラメーターを含むことができません。</span><span class="sxs-lookup"><span data-stu-id="9b5cd-120">The SELECT statement that defines the view cannot contain any parameters.</span></span>

<span data-ttu-id="9b5cd-121">ビュー名は、既存のテーブルと同じ名前にしないでください。</span><span class="sxs-lookup"><span data-stu-id="9b5cd-121">The name of the view cannot be the same as the name of an existing table.</span></span>

<span data-ttu-id="9b5cd-122">SELECT ステートメントによって定義されたクエリが更新可能な場合は、ビューも更新できます。</span><span class="sxs-lookup"><span data-stu-id="9b5cd-122">If the query defined by the SELECT statement is updatable, the view is also updatable.</span></span> <span data-ttu-id="9b5cd-123">それ以外の場合、ビューは読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="9b5cd-123">Otherwise, the view is read-only.</span></span>

<span data-ttu-id="9b5cd-124">SELECT ステートメントで定義されるクエリで 2 つのフィールドが同じ名前の場合、クエリでフィールドごとに一意の名前が指定されるフィールド リストを、ビューの定義に含む必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b5cd-124">If any two fields in the query defined by the SELECT statement have the same name, the view definition must include a field list specifying unique names for each of the fields in the query.</span></span>

