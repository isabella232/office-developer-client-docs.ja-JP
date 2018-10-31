---
title: ユーザーの変更、またはデータベースのステートメント (Microsoft Access SQL)
TOCTitle: ALTER USER or DATABASE statement (Microsoft Access SQL)
ms:assetid: 86ccd296-5171-97e7-683f-cdaab4bde9ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197012(v=office.15)
ms:contentKeyID: 48546093
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: ad03607b6452da016bad09fd33561bd811a2a16d
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862612"
---
# <a name="alter-user-or-database-statement-microsoft-access-sql"></a><span data-ttu-id="cf471-102">ユーザーの変更、またはデータベースのステートメント (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="cf471-102">ALTER USER or DATABASE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="cf471-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="cf471-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="cf471-104">既存のユーザーまたはデータベースのパスワードを変更します。</span><span class="sxs-lookup"><span data-stu-id="cf471-104">Changes the password for an existing user or for a database.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf471-105">構文</span><span class="sxs-lookup"><span data-stu-id="cf471-105">Syntax</span></span>

<span data-ttu-id="cf471-106">*Newpassword oldpassword*のデータベース パスワードの変更</span><span class="sxs-lookup"><span data-stu-id="cf471-106">ALTER DATABASE PASSWORD *newpassword oldpassword*</span></span>

<span data-ttu-id="cf471-107">ユーザーの変更*ユーザー*のパスワード*newpassword oldpassword*</span><span class="sxs-lookup"><span data-stu-id="cf471-107">ALTER USER *user* PASSWORD *newpassword oldpassword*</span></span>

<span data-ttu-id="cf471-108">ALTER USER ステートメントまたは DATABASE ステートメントには次の指定項目があります。</span><span class="sxs-lookup"><span data-stu-id="cf471-108">The ALTER USER or DATABASE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cf471-109">指定項目</span><span class="sxs-lookup"><span data-stu-id="cf471-109">Part</span></span></p></th>
<th><p><span data-ttu-id="cf471-110">説明</span><span class="sxs-lookup"><span data-stu-id="cf471-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cf471-111"><em>user</em></span><span class="sxs-lookup"><span data-stu-id="cf471-111"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="cf471-112">ワークグループ情報ファイルに追加されるユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="cf471-112">The name of a user to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf471-113"><em>newpassword</em></span><span class="sxs-lookup"><span data-stu-id="cf471-113"><em>newpassword</em></span></span></p></td>
<td><p><span data-ttu-id="cf471-114">指定した<em>ユーザー</em>名または<em>データベース</em>名に関連付けられる新しいパスワードです。</span><span class="sxs-lookup"><span data-stu-id="cf471-114">The new password to be associated with the specified <em>user</em> or <em>database</em> name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf471-115"><em>oldpassword</em></span><span class="sxs-lookup"><span data-stu-id="cf471-115"><em>oldpassword</em></span></span></p></td>
<td><p><span data-ttu-id="cf471-116">指定した<em>ユーザー</em>または<em>グループ</em>名に関連付けられる既存のパスワード。</span><span class="sxs-lookup"><span data-stu-id="cf471-116">The existing password to be associated with the specified <em>user</em> or <em>group</em> name.</span></span></p></td>
</tr>
</tbody>
</table>

