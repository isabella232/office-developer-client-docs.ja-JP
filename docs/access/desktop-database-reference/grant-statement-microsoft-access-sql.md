---
title: GRANT ステートメント (Microsoft Access SQL)
TOCTitle: GRANT Statement (Microsoft Access SQL)
ms:assetid: 50ae97ae-d5be-57e5-d9da-f3fc42f01d83
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193820(v=office.15)
ms:contentKeyID: 48544800
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277478
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d4fffc9ac40586be899de0dd4054ba39dd3a6489
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476229"
---
# <a name="grant-statement-microsoft-access-sql"></a><span data-ttu-id="cc811-102">GRANT ステートメント (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="cc811-102">GRANT Statement (Microsoft Access SQL)</span></span>


<span data-ttu-id="cc811-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="cc811-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="cc811-104">既存のユーザーまたはグループに与える権限を指定します。</span><span class="sxs-lookup"><span data-stu-id="cc811-104">Grants specific privileges to an existing user or group.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc811-105">構文</span><span class="sxs-lookup"><span data-stu-id="cc811-105">Syntax</span></span>

<span data-ttu-id="cc811-106">付与 {*特権*\[、*特権*、.\]} に {テーブル*テーブル*|オブジェクトの*オブジェクト*|</span><span class="sxs-lookup"><span data-stu-id="cc811-106">GRANT {*privilege*\[, *privilege*, …\]} ON{TABLE *table* | OBJECT *object*|</span></span>

<span data-ttu-id="cc811-107">コンテナー*コンテナー* } に {*authorizationname*\[、 *authorizationname*、.\]}</span><span class="sxs-lookup"><span data-stu-id="cc811-107">CONTAINER *container* } TO {*authorizationname*\[, *authorizationname*, …\]}</span></span>

<span data-ttu-id="cc811-108">GRANT ステートメントには、次の指定項目があります。</span><span class="sxs-lookup"><span data-stu-id="cc811-108">The GRANT statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cc811-109">指定項目</span><span class="sxs-lookup"><span data-stu-id="cc811-109">Part</span></span></p></th>
<th><p><span data-ttu-id="cc811-110">説明</span><span class="sxs-lookup"><span data-stu-id="cc811-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cc811-111"><em>privilege</em></span><span class="sxs-lookup"><span data-stu-id="cc811-111"><em>privilege</em></span></span></p></td>
<td><p><span data-ttu-id="cc811-112">特権または権限が与えられます。</span><span class="sxs-lookup"><span data-stu-id="cc811-112">The privilege or privileges to be granted.</span></span> <span data-ttu-id="cc811-113">次のキーワードを使用する権限を指定: 選択、削除、挿入、更新、削除、SELECTSECURITY、UPDATESECURITY、DBPASSWORD、UPDATEIDENTITY、作成、SELECTSCHEMA、スキーマおよび UPDATEOWNER。</span><span class="sxs-lookup"><span data-stu-id="cc811-113">Privileges are specified using the following keywords: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA and UPDATEOWNER.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc811-114"><em>tablename</em></span><span class="sxs-lookup"><span data-stu-id="cc811-114"><em>tablename</em></span></span></p></td>
<td><p><span data-ttu-id="cc811-115">任意の有効なテーブル名。</span><span class="sxs-lookup"><span data-stu-id="cc811-115">Any valid table name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc811-116"><em>object</em></span><span class="sxs-lookup"><span data-stu-id="cc811-116"><em>object</em></span></span></p></td>
<td><p><span data-ttu-id="cc811-p102">テーブル以外のどのオブジェクトも指定できます。たとえば、ストアド クエリ (ビューまたはプロシージャ) を指定できます。</span><span class="sxs-lookup"><span data-stu-id="cc811-p102">This can encompass any non-table object. A stored query (view or procedure) is one example.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc811-119"><em>container</em></span><span class="sxs-lookup"><span data-stu-id="cc811-119"><em>container</em></span></span></p></td>
<td><p><span data-ttu-id="cc811-120">有効なコンテナーの名前。</span><span class="sxs-lookup"><span data-stu-id="cc811-120">The name of a valid container.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc811-121"><em>authorizationname</em></span><span class="sxs-lookup"><span data-stu-id="cc811-121"><em>authorizationname</em></span></span></p></td>
<td><p><span data-ttu-id="cc811-122">ユーザー名またはグループ名。</span><span class="sxs-lookup"><span data-stu-id="cc811-122">A user or group name.</span></span></p></td>
</tr>
</tbody>
</table>

