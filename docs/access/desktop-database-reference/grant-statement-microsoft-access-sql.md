---
title: GRANT ステートメント (Microsoft Access SQL)
TOCTitle: GRANT statement (Microsoft Access SQL)
ms:assetid: 50ae97ae-d5be-57e5-d9da-f3fc42f01d83
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193820(v=office.15)
ms:contentKeyID: 48544800
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277478
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 4357099f8bcb9b2308b5cda3543949765b8c3420
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292133"
---
# <a name="grant-statement-microsoft-access-sql"></a><span data-ttu-id="fe580-102">GRANT ステートメント (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="fe580-102">GRANT statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="fe580-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="fe580-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fe580-104">既存のユーザーまたはグループに与える権限を指定します。</span><span class="sxs-lookup"><span data-stu-id="fe580-104">Grants specific privileges to an existing user or group.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe580-105">構文</span><span class="sxs-lookup"><span data-stu-id="fe580-105">Syntax</span></span>

<span data-ttu-id="fe580-106">付与 {*特権*\[,*特権*,...\]} {table *table* |object*オブジェクト*|</span><span class="sxs-lookup"><span data-stu-id="fe580-106">GRANT {*privilege*\[, *privilege*, …\]} ON{TABLE *table* | OBJECT *object*|</span></span>

<span data-ttu-id="fe580-107">container *container* } TO {*authorizationname*\[, *authorizationname*,...\]}</span><span class="sxs-lookup"><span data-stu-id="fe580-107">CONTAINER *container* } TO {*authorizationname*\[, *authorizationname*, …\]}</span></span>

<span data-ttu-id="fe580-108">GRANT ステートメントには、次の指定項目があります。</span><span class="sxs-lookup"><span data-stu-id="fe580-108">The GRANT statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fe580-109">パーツ</span><span class="sxs-lookup"><span data-stu-id="fe580-109">Part</span></span></p></th>
<th><p><span data-ttu-id="fe580-110">説明</span><span class="sxs-lookup"><span data-stu-id="fe580-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fe580-111"><em>オペレーター</em></span><span class="sxs-lookup"><span data-stu-id="fe580-111"><em>privilege</em></span></span></p></td>
<td><p><span data-ttu-id="fe580-112">権限を与えます。</span><span class="sxs-lookup"><span data-stu-id="fe580-112">The privilege or privileges to be granted.</span></span> <span data-ttu-id="fe580-113">権限は、SELECT、DELETE、INSERT、UPDATE、DROP、selectsecurity、UPDATESECURITY、dbpassword、UPDATEIDENTITY、CREATE、selectsecurity、schema、および updateowner の各キーワードを使用して指定します。</span><span class="sxs-lookup"><span data-stu-id="fe580-113">Privileges are specified using the following keywords: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA, and UPDATEOWNER.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe580-114"><em>tablename</em></span><span class="sxs-lookup"><span data-stu-id="fe580-114"><em>tablename</em></span></span></p></td>
<td><p><span data-ttu-id="fe580-115">任意の有効なテーブル名。</span><span class="sxs-lookup"><span data-stu-id="fe580-115">Any valid table name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe580-116"><em>object</em></span><span class="sxs-lookup"><span data-stu-id="fe580-116"><em>object</em></span></span></p></td>
<td><p><span data-ttu-id="fe580-117">テーブル以外のどのオブジェクトも指定できます。</span><span class="sxs-lookup"><span data-stu-id="fe580-117">This can encompass any non-table object.</span></span> <span data-ttu-id="fe580-118">たとえば、ストアド クエリ (ビューまたはプロシージャ) を指定できます。</span><span class="sxs-lookup"><span data-stu-id="fe580-118">A stored query (view or procedure) is one example.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe580-119"><em>格納</em></span><span class="sxs-lookup"><span data-stu-id="fe580-119"><em>container</em></span></span></p></td>
<td><p><span data-ttu-id="fe580-120">有効なコンテナーの名前。</span><span class="sxs-lookup"><span data-stu-id="fe580-120">The name of a valid container.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe580-121"><em>authorizationname</em></span><span class="sxs-lookup"><span data-stu-id="fe580-121"><em>authorizationname</em></span></span></p></td>
<td><p><span data-ttu-id="fe580-122">ユーザー名またはグループ名。</span><span class="sxs-lookup"><span data-stu-id="fe580-122">A user or group name.</span></span></p></td>
</tr>
</tbody>
</table>

