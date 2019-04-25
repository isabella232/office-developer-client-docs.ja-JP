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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295367"
---
# <a name="create-view-statement-microsoft-access-sql"></a><span data-ttu-id="ef459-102">CREATE VIEW ステートメント (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="ef459-102">CREATE VIEW Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="ef459-103">**適用先**: Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="ef459-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ef459-104">新しいビューを作成します。</span><span class="sxs-lookup"><span data-stu-id="ef459-104">Creates a new view.</span></span>

> [!NOTE]
> <span data-ttu-id="ef459-105">Microsoft Access データベース エンジンでは、Microsoft Access データベース エンジン以外のデータベースで CREATE VIEW やその他の DDL ステートメントを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="ef459-105">The Microsoft Access database engine does not support the use of CREATE VIEW, or any of the DDL statements, with non-Microsoft Access database engine databases.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef459-106">構文</span><span class="sxs-lookup"><span data-stu-id="ef459-106">Syntax</span></span>

<span data-ttu-id="ef459-107">CREATE VIEW *view* \[(*field1*\[, *field2*\[, …\]\])\] AS *selectstatement*</span><span class="sxs-lookup"><span data-stu-id="ef459-107">CREATE VIEW *view [(field1* \[[, *field2*[, …]])] AS *selectstatement*</span></span>

<span data-ttu-id="ef459-108">CREATE VIEW ステートメントでは、次の引数を使用します。</span><span class="sxs-lookup"><span data-stu-id="ef459-108">The CREATE VIEW statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ef459-109">パーツ</span><span class="sxs-lookup"><span data-stu-id="ef459-109">Part</span></span></p></th>
<th><p><span data-ttu-id="ef459-110">説明</span><span class="sxs-lookup"><span data-stu-id="ef459-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef459-111"><em>view</em></span><span class="sxs-lookup"><span data-stu-id="ef459-111"><em>view</em></span></span></p></td>
<td><p><span data-ttu-id="ef459-112">作成するビューの名前です。</span><span class="sxs-lookup"><span data-stu-id="ef459-112">The name of the view to be created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef459-113"><em>field1</em>、<em>field2</em></span><span class="sxs-lookup"><span data-stu-id="ef459-113"><em>field1</em>  ,  <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="ef459-114">
            <em>selectstatement</em> に指定されている該当フィールドのフィールド名です。</span><span class="sxs-lookup"><span data-stu-id="ef459-114">The name of field or fields for the corresponding fields specified in <em>selectstatement</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef459-115"><em>selectstatement</em></span><span class="sxs-lookup"><span data-stu-id="ef459-115"><em>selectstatement</em></span></span></p></td>
<td><p><span data-ttu-id="ef459-116">SQL SELECT ステートメントです。</span><span class="sxs-lookup"><span data-stu-id="ef459-116">A SQL SELECT statement.</span></span> <span data-ttu-id="ef459-117">詳細については、「<a href="select-statement-microsoft-access-sql.md">SELECT ステートメント</a>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ef459-117">For more information, see <a href="select-statement-microsoft-access-sql.md">SELECT Statement</a>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="ef459-118">注釈</span><span class="sxs-lookup"><span data-stu-id="ef459-118">Remarks</span></span>

<span data-ttu-id="ef459-119">ビューを定義するのは SELECT ステートメントであり、[SELECT...INTO](select-into-statement-microsoft-access-sql.md) ステートメントではありません。</span><span class="sxs-lookup"><span data-stu-id="ef459-119">The SELECT statement that defines the view cannot be a [SELECT INTO](select-into-statement-microsoft-access-sql.md) statement.</span></span>

<span data-ttu-id="ef459-120">ビューを定義する SELECT ステートメントには、パラメーターを含めることができません。</span><span class="sxs-lookup"><span data-stu-id="ef459-120">The SELECT statement that defines the view cannot contain any parameters.</span></span>

<span data-ttu-id="ef459-121">ビューの名前は、既存のテーブルの名前と同じにすることができません。</span><span class="sxs-lookup"><span data-stu-id="ef459-121">The name of the view cannot be the same as the name of an existing table.</span></span>

<span data-ttu-id="ef459-122">SELECT ステートメントによって定義されたクエリが更新できる場合、ビューも更新できます。</span><span class="sxs-lookup"><span data-stu-id="ef459-122">If the query defined by the SELECT statement is updatable, then the view is also updatable. Otherwise, the view is read-only.</span></span> <span data-ttu-id="ef459-123">更新できない場合、ビューは読み取り専用となります。</span><span class="sxs-lookup"><span data-stu-id="ef459-123">Otherwise, the classic view is rendered.</span></span>

<span data-ttu-id="ef459-124">SELECT ステートメントで定義されるクエリに名前が同じフィールドが 2 つある場合、ビューの定義にフィールド リストを追加し、クエリの各フィールドに一意の名前を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef459-124">If any two fields in the query defined by the SELECT statement have the same name, the view definition must include a field list specifying unique names for each of the fields in the query.</span></span>

