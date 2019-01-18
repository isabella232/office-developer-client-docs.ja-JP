---
title: カスタマイズ ファイルの UserList セクション
TOCTitle: Customization File UserList section
ms:assetid: b60ba3b0-37d4-bb59-d3cd-2ab44d178b8a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249873(v=office.15)
ms:contentKeyID: 48547263
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ecaf77765051a202925449d0221f0a68a2a06622
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721501"
---
# <a name="customization-file-userlist-section"></a><span data-ttu-id="5b627-102">カスタマイズ ファイルの UserList セクション</span><span class="sxs-lookup"><span data-stu-id="5b627-102">Customization File UserList section</span></span>


<span data-ttu-id="5b627-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="5b627-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5b627-104">**Userlist**セクションは、同じセクション*の識別子*パラメーターを使用して、[**接続**] セクションに関係します。</span><span class="sxs-lookup"><span data-stu-id="5b627-104">The **userlist** section pertains to the **connect** section with the same section *identifier* parameter.</span></span>

<span data-ttu-id="5b627-105">このセクションでは、*ユーザー アクセス エントリ*を指定したユーザーのアクセス権を指定し、一致する [**接続**] セクションで*既定*の*アクセス エントリ*をオーバーライドを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="5b627-105">This section can contain a *user access entry*, which specifies access rights for the specified user and overrides the *default* *access entry* in the matching **connect** section.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b627-106">構文</span><span class="sxs-lookup"><span data-stu-id="5b627-106">Syntax</span></span>

<span data-ttu-id="5b627-107">ユーザー アクセス エントリの形式は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="5b627-107">A user access entry is of the form:</span></span>

<span data-ttu-id="5b627-108">*ユーザー名。 =*・ アクセス権。</span><span class="sxs-lookup"><span data-stu-id="5b627-108">*userName\*\*\*=* accessRights\*\*\*</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5b627-109">指定項目</span><span class="sxs-lookup"><span data-stu-id="5b627-109">Part</span></span></p></th>
<th><p><span data-ttu-id="5b627-110">説明</span><span class="sxs-lookup"><span data-stu-id="5b627-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5b627-111"><em>userName</em></span><span class="sxs-lookup"><span data-stu-id="5b627-111"><em>userName</em></span></span></p></td>
<td><p><span data-ttu-id="5b627-112">この接続を使用しているユーザーの<em>ユーザー名</em>です。</span><span class="sxs-lookup"><span data-stu-id="5b627-112">The <em>user name</em> of the person employing this connection.</span></span> <span data-ttu-id="5b627-113">IIS<strong>サービス マネージャー</strong>のダイアログ ボックスは、有効なユーザー名が確立されます。</span><span class="sxs-lookup"><span data-stu-id="5b627-113">Valid user names are established with the IIS <strong>Service Manager</strong> dialog.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b627-114"><strong><em>・ アクセス権</em></strong></span><span class="sxs-lookup"><span data-stu-id="5b627-114"><strong><em>accessRights</em></strong></span></span></p></td>
<td><p><span data-ttu-id="5b627-115">次のアクセス権のいずれかを指定します。
</span><span class="sxs-lookup"><span data-stu-id="5b627-115">One of the following access rights:</span></span><br />
</p>
<ul>
<li><p><span data-ttu-id="5b627-116"><strong>NoAccess</strong> ユーザーは、データ ソースにアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="5b627-116"><strong>NoAccess</strong> — User cannot access the data source.</span></span></p></li>
<li><p><span data-ttu-id="5b627-117"><strong>ReadOnly</strong> ユーザーは、データ ソースの読み取りが可能です。</span><span class="sxs-lookup"><span data-stu-id="5b627-117"><strong>ReadOnly</strong> — User can read the data source.</span></span></p></li>
<li><p><span data-ttu-id="5b627-118"><strong>ReadWrite</strong> ユーザーは、データ ソースの読み取り/書き込みが可能です。</span><span class="sxs-lookup"><span data-stu-id="5b627-118"><strong>ReadWrite</strong> — User can read or write to the data source.</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>

