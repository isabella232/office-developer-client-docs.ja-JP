---
title: CREATE VIEW ステートメント (Microsoft Access SQL)
TOCTitle: CREATE VIEW Statement (Microsoft Access SQL)
ms:assetid: ecaabd75-3081-fd35-830d-5a59b0a51922
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836312(v=office.15)
ms:contentKeyID: 48548519
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 292dddeab15c71fb188a928ac0e491063930214d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477371"
---
# <a name="create-view-statement-microsoft-access-sql"></a><span data-ttu-id="27089-102">CREATE VIEW ステートメント (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="27089-102">CREATE VIEW Statement (Microsoft Access SQL)</span></span>


<span data-ttu-id="27089-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="27089-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="27089-104">新しいビューを作成します。</span><span class="sxs-lookup"><span data-stu-id="27089-104">Creates a new view.</span></span>


> [!NOTE]
> <P><span data-ttu-id="27089-105">[!メモ] Microsoft Access データベース エンジンは、Microsoft Access データベース エンジン以外のデータベースでは CREATE VIEW 句や DDL (データ定義言語) ステートメントを使用できません。</span><span class="sxs-lookup"><span data-stu-id="27089-105">The Microsoft Access database engine does not support the use of CREATE VIEW, or any of the DDL statements, with non-Microsoft Access database engine databases.</span></span></P>



## <a name="syntax"></a><span data-ttu-id="27089-106">構文</span><span class="sxs-lookup"><span data-stu-id="27089-106">Syntax</span></span>

<span data-ttu-id="27089-107">*ビュー*のビューの作成\[(*フィールド 1*\[、*フィールド 2*\[、.\] \])\]として*使いましょう*</span><span class="sxs-lookup"><span data-stu-id="27089-107">CREATE VIEW *view* \[(*field1*\[, *field2*\[, …\]\])\] AS *selectstatement*</span></span>

<span data-ttu-id="27089-108">CREATE VIEW ステートメントには次の指定項目があります。</span><span class="sxs-lookup"><span data-stu-id="27089-108">The CREATE VIEW statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="27089-109">指定項目</span><span class="sxs-lookup"><span data-stu-id="27089-109">Part</span></span></p></th>
<th><p><span data-ttu-id="27089-110">説明</span><span class="sxs-lookup"><span data-stu-id="27089-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="27089-111"><em>view</em></span><span class="sxs-lookup"><span data-stu-id="27089-111"><em>view</em></span></span></p></td>
<td><p><span data-ttu-id="27089-112">作成するビューの名前。</span><span class="sxs-lookup"><span data-stu-id="27089-112">The name of the view to be created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27089-113"><em>field1</em>, <em>field2</em></span><span class="sxs-lookup"><span data-stu-id="27089-113"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="27089-114"><em>selectstatement</em> で指定された関連フィールドのフィールド名。</span><span class="sxs-lookup"><span data-stu-id="27089-114">The name of field or fields for the corresponding fields specified in <em>selectstatement</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27089-115"><em>selectstatement</em></span><span class="sxs-lookup"><span data-stu-id="27089-115"><em>selectstatement</em></span></span></p></td>
<td><p><span data-ttu-id="27089-p101">SQL SELECT ステートメント。詳細については、「<a href="select-statement-microsoft-access-sql.md">SELECT ステートメント</a>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="27089-p101">A SQL SELECT statement. For more information, see <a href="select-statement-microsoft-access-sql.md">SELECT Statement</a>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="27089-118">解説</span><span class="sxs-lookup"><span data-stu-id="27089-118">Remarks</span></span>

<span data-ttu-id="27089-119">ビューを定義するのは SELECT ステートメントであり、[SELECT...INTO](select-into-statement-microsoft-access-sql.md) ステートメントではありません。</span><span class="sxs-lookup"><span data-stu-id="27089-119">The SELECT statement that defines the view cannot be a [SELECT INTO](select-into-statement-microsoft-access-sql.md) statement.</span></span>

<span data-ttu-id="27089-120">ビューを定義する SELECT ステートメントは、パラメーターを含むことができません。</span><span class="sxs-lookup"><span data-stu-id="27089-120">The SELECT statement that defines the view cannot contain any parameters.</span></span>

<span data-ttu-id="27089-121">ビュー名は、既存のテーブルと同じ名前にしないでください。</span><span class="sxs-lookup"><span data-stu-id="27089-121">The name of the view cannot be the same as the name of an existing table.</span></span>

<span data-ttu-id="27089-p102">SELECT ステートメントで定義されたクエリが更新されると、読み取り専用に設定されていない限り、ビューも更新されます。</span><span class="sxs-lookup"><span data-stu-id="27089-p102">If the query defined by the SELECT statement is updatable, then the view is also updatable. Otherwise, the view is read-only.</span></span>

<span data-ttu-id="27089-124">SELECT ステートメントで定義されるクエリで 2 つのフィールドが同じ名前の場合、クエリでフィールドごとに一意の名前が指定されるフィールド リストを、ビューの定義に含む必要があります。</span><span class="sxs-lookup"><span data-stu-id="27089-124">If any two fields in the query defined by the SELECT statement have the same name, the view definition must include a field list specifying unique names for each of the fields in the query.</span></span>

