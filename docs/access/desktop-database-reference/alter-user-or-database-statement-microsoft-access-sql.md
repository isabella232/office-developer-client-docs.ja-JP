---
title: ユーザーの変更、またはデータベースのステートメント (Microsoft Access SQL)
TOCTitle: ALTER USER or DATABASE statement (Microsoft Access SQL)
ms:assetid: 86ccd296-5171-97e7-683f-cdaab4bde9ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197012(v=office.15)
ms:contentKeyID: 48546093
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2514ca6403ce70acae9e344d610fbd7b9ba7d73b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702286"
---
# <a name="alter-user-or-database-statement-microsoft-access-sql"></a><span data-ttu-id="fb449-102">ユーザーの変更、またはデータベースのステートメント (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="fb449-102">ALTER USER or DATABASE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="fb449-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="fb449-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fb449-104">既存のユーザーまたはデータベースのパスワードを変更します。</span><span class="sxs-lookup"><span data-stu-id="fb449-104">Changes the password for an existing user or for a database.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb449-105">構文</span><span class="sxs-lookup"><span data-stu-id="fb449-105">Syntax</span></span>

<span data-ttu-id="fb449-106">*Newpassword oldpassword*のデータベース パスワードの変更</span><span class="sxs-lookup"><span data-stu-id="fb449-106">ALTER DATABASE PASSWORD *newpassword oldpassword*</span></span>

<span data-ttu-id="fb449-107">ユーザーの変更*ユーザー*のパスワード*newpassword oldpassword*</span><span class="sxs-lookup"><span data-stu-id="fb449-107">ALTER USER *user* PASSWORD *newpassword oldpassword*</span></span>

<span data-ttu-id="fb449-108">ALTER USER ステートメントまたは DATABASE ステートメントには次の指定項目があります。</span><span class="sxs-lookup"><span data-stu-id="fb449-108">The ALTER USER or DATABASE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fb449-109">指定項目</span><span class="sxs-lookup"><span data-stu-id="fb449-109">Part</span></span></p></th>
<th><p><span data-ttu-id="fb449-110">説明</span><span class="sxs-lookup"><span data-stu-id="fb449-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fb449-111"><em>user</em></span><span class="sxs-lookup"><span data-stu-id="fb449-111"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="fb449-112">ワークグループ情報ファイルに追加されるユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="fb449-112">The name of a user to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb449-113"><em>newpassword</em></span><span class="sxs-lookup"><span data-stu-id="fb449-113"><em>newpassword</em></span></span></p></td>
<td><p><span data-ttu-id="fb449-114">指定した<em>ユーザー</em>名または<em>データベース</em>名に関連付けられる新しいパスワードです。</span><span class="sxs-lookup"><span data-stu-id="fb449-114">The new password to be associated with the specified <em>user</em> or <em>database</em> name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb449-115"><em>oldpassword</em></span><span class="sxs-lookup"><span data-stu-id="fb449-115"><em>oldpassword</em></span></span></p></td>
<td><p><span data-ttu-id="fb449-116">指定した<em>ユーザー</em>または<em>グループ</em>名に関連付けられる既存のパスワード。</span><span class="sxs-lookup"><span data-stu-id="fb449-116">The existing password to be associated with the specified <em>user</em> or <em>group</em> name.</span></span></p></td>
</tr>
</tbody>
</table>

