---
title: ステートメント (Microsoft Access SQL) を失効させる
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
ms.openlocfilehash: 4bcdd7aa77823a53ba2a2c0cde4badbac571611a
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860547"
---
# <a name="revoke-statement-microsoft-access-sql"></a><span data-ttu-id="fd445-102">ステートメント (Microsoft Access SQL) を失効させる</span><span class="sxs-lookup"><span data-stu-id="fd445-102">REVOKE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="fd445-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="fd445-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="fd445-104">既存のユーザーまたはグループから、指定の権限を無効にします。</span><span class="sxs-lookup"><span data-stu-id="fd445-104">Revokes specific privileges from an existing user or group.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd445-105">構文</span><span class="sxs-lookup"><span data-stu-id="fd445-105">Syntax</span></span>

<span data-ttu-id="fd445-106">取り消し {*特権*\[、*特権*、.\]} に {テーブル*テーブル*|オブジェクトの*オブジェクト*|</span><span class="sxs-lookup"><span data-stu-id="fd445-106">REVOKE {*privilege*\[, *privilege*, …\]} ON {TABLE *table* | OBJECT *object*|</span></span>

<span data-ttu-id="fd445-107">コンテナー*コンテナー*} から {*authorizationname*\[、 *authorizationname*、.\]}</span><span class="sxs-lookup"><span data-stu-id="fd445-107">CONTAINTER *container*} FROM {*authorizationname*\[, *authorizationname*, …\]}</span></span>

<span data-ttu-id="fd445-108">REVOKE ステートメントには、次の指定項目があります。</span><span class="sxs-lookup"><span data-stu-id="fd445-108">The REVOKE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fd445-109">指定項目</span><span class="sxs-lookup"><span data-stu-id="fd445-109">Part</span></span></p></th>
<th><p><span data-ttu-id="fd445-110">説明</span><span class="sxs-lookup"><span data-stu-id="fd445-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fd445-111"><em>privilege</em></span><span class="sxs-lookup"><span data-stu-id="fd445-111"><em>privilege</em></span></span></p></td>
<td><p><span data-ttu-id="fd445-112">権限または特権を無効にします。</span><span class="sxs-lookup"><span data-stu-id="fd445-112">The privilege or privileges to be revoked.</span></span> <span data-ttu-id="fd445-113">次のキーワードを使用する権限を指定します。] を選択、削除、挿入、更新、ドロップ、SELECTSECURITY、UPDATESECURITY、DBPASSWORD、UPDATEIDENTITY、作成、SELECTSCHEMA、スキーマ、および UPDATEOWNER。</span><span class="sxs-lookup"><span data-stu-id="fd445-113">Privileges are specified using the following keywords: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA, and UPDATEOWNER.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd445-114"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="fd445-114"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="fd445-115">任意の有効なテーブル名。</span><span class="sxs-lookup"><span data-stu-id="fd445-115">Any valid table name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd445-116"><em>object</em></span><span class="sxs-lookup"><span data-stu-id="fd445-116"><em>object</em></span></span></p></td>
<td><p><span data-ttu-id="fd445-p102">テーブル以外のどのオブジェクトも指定できます。たとえば、ストアド クエリ (ビューまたはプロシージャ) を指定できます。</span><span class="sxs-lookup"><span data-stu-id="fd445-p102">This can encompass any non-table object. A stored query (view or procedure) is one example.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd445-119"><em>container</em></span><span class="sxs-lookup"><span data-stu-id="fd445-119"><em>container</em></span></span></p></td>
<td><p><span data-ttu-id="fd445-120">有効なコンテナーの名前。</span><span class="sxs-lookup"><span data-stu-id="fd445-120">The name of a valid container.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd445-121"><em>authorizationname</em></span><span class="sxs-lookup"><span data-stu-id="fd445-121"><em>authorizationname</em></span></span></p></td>
<td><p><span data-ttu-id="fd445-122">ユーザー名またはグループ名。</span><span class="sxs-lookup"><span data-stu-id="fd445-122">A user or group name.</span></span></p></td>
</tr>
</tbody>
</table>

