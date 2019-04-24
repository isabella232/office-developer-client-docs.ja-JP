---
title: カスタマイズ ファイルの概要
TOCTitle: Understanding the Customization File
ms:assetid: 98fd5ec1-d5bd-cdd2-5eb5-9a1682fbed79
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249686(v=office.15)
ms:contentKeyID: 48546507
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b977fc4273068ac52efe8960761a9e28a6234e2e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314071"
---
# <a name="understanding-the-customization-file"></a><span data-ttu-id="e2025-102">カスタマイズ ファイルの概要</span><span class="sxs-lookup"><span data-stu-id="e2025-102">Understanding the Customization File</span></span>


<span data-ttu-id="e2025-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="e2025-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e2025-104">カスタマイズファイルの各セクションヘッダーは、type と parameter を**\[** 含む角かっこ () で構成されています。</span><span class="sxs-lookup"><span data-stu-id="e2025-104">Each section header in the customization file consists of square brackets (**\[\]**) containing a type and parameter.</span></span> <span data-ttu-id="e2025-105">4つのセクションの種類は、リテラル文字列**connect**、 **sql**、 **userlist**、または**logs**で示されます。</span><span class="sxs-lookup"><span data-stu-id="e2025-105">The four section types are indicated by the literal strings **connect**, **sql**, **userlist**, or **logs**.</span></span> <span data-ttu-id="e2025-106">パラメーターは、リテラル文字列、既定値、ユーザー指定の識別子、または何も指定されていません。</span><span class="sxs-lookup"><span data-stu-id="e2025-106">The parameter is the literal string, the default, a user-specified identifier, or nothing.</span></span>

<span data-ttu-id="e2025-107">つまり、各セクションは以下のセクション ヘッダーのいずれかで示されます。</span><span class="sxs-lookup"><span data-stu-id="e2025-107">Therefore, each section is marked with one of the following section headers:</span></span>

```text 
 
[ connect   default     ]
[ connect   identifier  ]
[ sql       default     ]
[ sql       identifier  ]
[ userlist  identifier  ]
[ logs                  ]
```

<span data-ttu-id="e2025-108">セクション ヘッダーには以下の要素があります。</span><span class="sxs-lookup"><span data-stu-id="e2025-108">The section headers have the following parts.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e2025-109">パーツ</span><span class="sxs-lookup"><span data-stu-id="e2025-109">Part</span></span></p></th>
<th><p><span data-ttu-id="e2025-110">説明</span><span class="sxs-lookup"><span data-stu-id="e2025-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e2025-111"><strong>結び付ける</strong></span><span class="sxs-lookup"><span data-stu-id="e2025-111"><strong>connect</strong></span></span></p></td>
<td><p><span data-ttu-id="e2025-112">接続文字列を変更するリテラル文字列です。</span><span class="sxs-lookup"><span data-stu-id="e2025-112">A literal string that modifies a connection string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2025-113"><strong>sql</strong></span><span class="sxs-lookup"><span data-stu-id="e2025-113"><strong>sql</strong></span></span></p></td>
<td><p><span data-ttu-id="e2025-114">コマンド文字列を変更するリテラル文字列です。</span><span class="sxs-lookup"><span data-stu-id="e2025-114">A literal string that modifies a command string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2025-115"><strong>userlist</strong></span><span class="sxs-lookup"><span data-stu-id="e2025-115"><strong>userlist</strong></span></span></p></td>
<td><p><span data-ttu-id="e2025-116">特定のユーザーのアクセス権を変更するリテラル文字列です。</span><span class="sxs-lookup"><span data-stu-id="e2025-116">A literal string that modifies the access rights of a specific user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2025-117"><strong>ログ</strong></span><span class="sxs-lookup"><span data-stu-id="e2025-117"><strong>logs</strong></span></span></p></td>
<td><p><span data-ttu-id="e2025-118">操作エラーを記録するログ ファイルを指定するリテラル文字列です。</span><span class="sxs-lookup"><span data-stu-id="e2025-118">A literal string that specifies a log file recording operational errors.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2025-119"><strong>default</strong></span><span class="sxs-lookup"><span data-stu-id="e2025-119"><strong>default</strong></span></span></p></td>
<td><p><span data-ttu-id="e2025-120">識別子が指定されていない場合、または検出されない場合に使用されるリテラル文字列です。</span><span class="sxs-lookup"><span data-stu-id="e2025-120">A literal string that is used if no identifier is specified or found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2025-121"><em>識別子</em></span><span class="sxs-lookup"><span data-stu-id="e2025-121"><em>identifier</em></span></span></p></td>
<td><p><span data-ttu-id="e2025-122">"接続" 文字列または "コマンド" 文字列内の文字列と一致する文字列です。</span><span class="sxs-lookup"><span data-stu-id="e2025-122">A string that matches a string in the <strong>connect</strong> or <strong>command</strong> string.</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="e2025-123">セクション ヘッダーに <strong>connect</strong> があり、識別子の文字列が接続文字列内にある場合は、connect セクションが使用されます。</span><span class="sxs-lookup"><span data-stu-id="e2025-123">Use this section if the section header contains <strong>connect</strong> and the identifier string is found in the connection string.</span></span></p></li>
<li><p><span data-ttu-id="e2025-124">セクション ヘッダーに <strong>sql</strong> があり、識別子の文字列がコマンド文字列内にある場合は、sql セクションが使用されます。</span><span class="sxs-lookup"><span data-stu-id="e2025-124">Use this section if the section header contains <strong>sql</strong> and the identifier string is found in the command string.</span></span></p></li>
<li><p><span data-ttu-id="e2025-125">セクション ヘッダーに <strong>userlist</strong> があり、識別子の文字列が <strong>connect</strong> セクションの識別子と一致する場合は、userlist セクションが使用されます。</span><span class="sxs-lookup"><span data-stu-id="e2025-125">Use this section if the section header contains <strong>userlist</strong> and the identifier string matches a <strong>connect</strong> section identifier.</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e2025-p102">**DataFactory** はハンドラーを呼び出し、クライアントのパラメーターを渡します。ハンドラーは、クライアント パラメーター内の文字列全体を対象として、該当するセクション ヘッダー内の識別子と一致する文字列を検索します。一致する文字列が見つかると、そのセクションの内容がクライアント パラメーターに適用されます。</span><span class="sxs-lookup"><span data-stu-id="e2025-p102">The **DataFactory** calls the handler, passing client parameters. The handler searches for whole strings in the client parameters that match identifiers in the appropriate section headers. If a match is found, the contents of that section are applied to the client parameter.</span></span>

<span data-ttu-id="e2025-129">各セクションは次の状況下で使用されます。</span><span class="sxs-lookup"><span data-stu-id="e2025-129">A particular section is used under the following circumstances:</span></span>

  - <span data-ttu-id="e2025-130">connect \*\*\*\* セクションは、クライアントの connect 文字列キーワードの値の部分が "\**Data Source = \* \* \* value*" で、 **connect**セクションの識別子と一致する場合に使用され*ます。*</span><span class="sxs-lookup"><span data-stu-id="e2025-130">A **connect** section is used if the value part of the client connect string keyword, "\**Data Source=\*\*\*value*", matches a **connect** section identifier *.*</span></span>

  - <span data-ttu-id="e2025-131">**sql** セクションは、クライアントのコマンド文字列が **sql** セクションの識別子と一致する文字列を含んでいる場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="e2025-131">An **sql** section is used if the client command string contains a string that matches an **sql** section identifier.</span></span>

  - <span data-ttu-id="e2025-132">一致する識別子が存在しない場合は、既定のパラメーターを持つ **connect** セクションまたは **sql** セクションが使用されます。</span><span class="sxs-lookup"><span data-stu-id="e2025-132">A **connect** or **sql** section with a default parameter is used if there is no matching identifier.</span></span>

  - <span data-ttu-id="e2025-p103">**userlist** セクションは、 **userlist** セクションの識別子が **connect** セクションの識別子と一致する場合に使用されます。一致する場合は、 **userlist** セクションの内容が、 **connect** セクションによって管理される接続に適用されます。</span><span class="sxs-lookup"><span data-stu-id="e2025-p103">A **userlist** section is used if the **userlist** section identifier matches a **connect** section identifier. If there is a match, the contents of the **userlist** section are applied to the connection governed by the **connect** section.</span></span>

  - <span data-ttu-id="e2025-135">接続文字列またはコマンド文字列中の文字列がどの **connect** セクション ヘッダーまたは **sql** セクション ヘッダーの識別子とも一致せず、また、既定のパラメーターを持つ **connect** セクション ヘッダーまたは **sql** セクション ヘッダーがない場合は、クライアント文字列がそのまま使用されます。</span><span class="sxs-lookup"><span data-stu-id="e2025-135">If the string in a connection or command string does not match the identifier in any **connect** or **sql** section header, and there is no **connect** or **sql** section header with a default parameter, then the client string is used without modification.</span></span>

  - <span data-ttu-id="e2025-136">**logs** セクションは、 **DataFactory** の動作中に常に使用されます。</span><span class="sxs-lookup"><span data-stu-id="e2025-136">The **logs** section is used whenever the **DataFactory** is in operation.</span></span>

