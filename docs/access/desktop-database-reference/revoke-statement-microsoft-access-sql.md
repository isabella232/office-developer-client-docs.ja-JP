---
title: REVOKE ステートメント (Microsoft Access SQL)
TOCTitle: REVOKE statement (Microsoft Access SQL)
ms:assetid: 69399fd6-c4e8-f2e2-e5f4-48ae779323f5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195272(v=office.15)
ms:contentKeyID: 48545409
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277479
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 20122fee617597987940766a076d5f968a87c2d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306532"
---
# <a name="revoke-statement-microsoft-access-sql"></a><span data-ttu-id="ef92a-102">REVOKE ステートメント (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="ef92a-102">REVOKE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="ef92a-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="ef92a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ef92a-104">既存のユーザーまたはグループから、指定の権限を無効にします。</span><span class="sxs-lookup"><span data-stu-id="ef92a-104">Revokes specific privileges from an existing user or group.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef92a-105">構文</span><span class="sxs-lookup"><span data-stu-id="ef92a-105">Syntax</span></span>

<span data-ttu-id="ef92a-106">REVOKE {*privilege*\[,*特権*,...\]} {table *table* |object*オブジェクト*|</span><span class="sxs-lookup"><span data-stu-id="ef92a-106">REVOKE {*privilege*\[, *privilege*, …\]} ON {TABLE *table* | OBJECT *object*|</span></span>

<span data-ttu-id="ef92a-107">{*authorizationname*\[, *authorizationname*,... \*\*\]}</span><span class="sxs-lookup"><span data-stu-id="ef92a-107">CONTAINTER *container*} FROM {*authorizationname*\[, *authorizationname*, …\]}</span></span>

<span data-ttu-id="ef92a-108">REVOKE ステートメントには、次の指定項目があります。</span><span class="sxs-lookup"><span data-stu-id="ef92a-108">The REVOKE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ef92a-109">パーツ</span><span class="sxs-lookup"><span data-stu-id="ef92a-109">Part</span></span></p></th>
<th><p><span data-ttu-id="ef92a-110">説明</span><span class="sxs-lookup"><span data-stu-id="ef92a-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef92a-111"><em>オペレーター</em></span><span class="sxs-lookup"><span data-stu-id="ef92a-111"><em>privilege</em></span></span></p></td>
<td><p><span data-ttu-id="ef92a-112">権限を無効にします。</span><span class="sxs-lookup"><span data-stu-id="ef92a-112">The privilege or privileges to be revoked.</span></span> <span data-ttu-id="ef92a-113">権限は、SELECT、DELETE、INSERT、UPDATE、DROP、selectsecurity、UPDATESECURITY、dbpassword、UPDATEIDENTITY、CREATE、selectsecurity、schema、および updateowner の各キーワードを使用して指定します。</span><span class="sxs-lookup"><span data-stu-id="ef92a-113">Privileges are specified using the following keywords: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA, and UPDATEOWNER.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef92a-114"><em>テーブル</em></span><span class="sxs-lookup"><span data-stu-id="ef92a-114"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="ef92a-115">任意の有効なテーブル名。</span><span class="sxs-lookup"><span data-stu-id="ef92a-115">Any valid table name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef92a-116"><em>object</em></span><span class="sxs-lookup"><span data-stu-id="ef92a-116"><em>object</em></span></span></p></td>
<td><p><span data-ttu-id="ef92a-117">テーブル以外のどのオブジェクトも指定できます。</span><span class="sxs-lookup"><span data-stu-id="ef92a-117">This can encompass any non-table object.</span></span> <span data-ttu-id="ef92a-118">たとえば、ストアド クエリ (ビューまたはプロシージャ) を指定できます。</span><span class="sxs-lookup"><span data-stu-id="ef92a-118">A stored query (view or procedure) is one example.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef92a-119"><em>格納</em></span><span class="sxs-lookup"><span data-stu-id="ef92a-119"><em>container</em></span></span></p></td>
<td><p><span data-ttu-id="ef92a-120">有効なコンテナーの名前。</span><span class="sxs-lookup"><span data-stu-id="ef92a-120">The name of a valid container.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef92a-121"><em>authorizationname</em></span><span class="sxs-lookup"><span data-stu-id="ef92a-121"><em>authorizationname</em></span></span></p></td>
<td><p><span data-ttu-id="ef92a-122">ユーザー名またはグループ名。</span><span class="sxs-lookup"><span data-stu-id="ef92a-122">A user or group name.</span></span></p></td>
</tr>
</tbody>
</table>

