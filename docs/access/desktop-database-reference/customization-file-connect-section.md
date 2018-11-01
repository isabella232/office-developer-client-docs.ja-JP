---
title: カスタマイズ ファイルの Connect セクション
TOCTitle: Customization File Connect Section
ms:assetid: 037abfb4-798d-4b09-6133-356969aee95c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248802(v=office.15)
ms:contentKeyID: 48542985
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f160fe06167cde6527b08c23ab3de69731f56dde
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867523"
---
# <a name="customization-file-connect-section"></a><span data-ttu-id="a7419-102">カスタマイズ ファイルの Connect セクション</span><span class="sxs-lookup"><span data-stu-id="a7419-102">Customization File Connect Section</span></span>

<span data-ttu-id="a7419-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="a7419-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a7419-p101">ハンドラーの既定の動作では、すべての接続が拒否されます。 **connect** セクションで、この動作の例外を指定します。たとえば、 **connect** セクションが 1 つもないか、あっても空の場合、既定では接続は行われません。</span><span class="sxs-lookup"><span data-stu-id="a7419-p101">The default behavior of the handler is to deny all connections. The **connect** section specifies exceptions to that behavior. For example, if all the **connect** sections were absent or empty, then by default no connections could be made.</span></span>

<span data-ttu-id="a7419-107">**connect** セクションには、次のものを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="a7419-107">The **connect** section can contain:</span></span>

- <span data-ttu-id="a7419-p102">この接続で実行できる既定の読み取り/書き込み操作を指定する、既定のアクセス エントリ。このセクションに既定のアクセス エントリが存在しない場合、このセクションは無視されます。</span><span class="sxs-lookup"><span data-stu-id="a7419-p102">A default access entry that specifies the default read and write operations allowed on this connection. If there is no default access entry in the section, the section will be ignored.</span></span>

- <span data-ttu-id="a7419-110">クライアントの接続文字列を置き換える新しい接続文字列。</span><span class="sxs-lookup"><span data-stu-id="a7419-110">A new connection string that replaces the client connection string.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7419-111">構文</span><span class="sxs-lookup"><span data-stu-id="a7419-111">Syntax</span></span>

<span data-ttu-id="a7419-112">既定のアクセス エントリの形式は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="a7419-112">A default access entry is of the form:</span></span>

`Access=accessRight`

<span data-ttu-id="a7419-113">置き換える接続文字列エントリの形式は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="a7419-113">A replacement connection string entry is of the form:</span></span>

`Connect=connectionString`

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a7419-114">引数</span><span class="sxs-lookup"><span data-stu-id="a7419-114">Part</span></span></p></th>
<th><p><span data-ttu-id="a7419-115">説明</span><span class="sxs-lookup"><span data-stu-id="a7419-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a7419-116"><strong>Connect</strong></span><span class="sxs-lookup"><span data-stu-id="a7419-116"><strong>Connect</strong></span></span></p></td>
<td><p><span data-ttu-id="a7419-117">これが接続文字列のエントリであることを示すリテラル文字列。</span><span class="sxs-lookup"><span data-stu-id="a7419-117">A literal string that indicates this is a connection string entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7419-118"><strong><em>接続文字列</em></strong></span><span class="sxs-lookup"><span data-stu-id="a7419-118"><strong><em>connectionString</em></strong></span></span></p></td>
<td><p><span data-ttu-id="a7419-119">クライアントのすべての接続文字列を置き換える文字列。</span><span class="sxs-lookup"><span data-stu-id="a7419-119">A string that replaces the whole client connection string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a7419-120"><strong>Access</strong></span><span class="sxs-lookup"><span data-stu-id="a7419-120"><strong>Access</strong></span></span></p></td>
<td><p><span data-ttu-id="a7419-121">これがアクセス エントリであることを示すリテラル文字列。</span><span class="sxs-lookup"><span data-stu-id="a7419-121">A literal string that indicates this is an access entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7419-122"><strong><em>アクセス権</em></strong></span><span class="sxs-lookup"><span data-stu-id="a7419-122"><strong><em>accessRight</em></strong></span></span></p></td>
<td><p><span data-ttu-id="a7419-123">次のアクセス権のいずれかを指定します。
</span><span class="sxs-lookup"><span data-stu-id="a7419-123">One of the following access rights:</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="a7419-124"><strong>NoAccess</strong> ユーザーは、データ ソースにアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="a7419-124"><strong>NoAccess</strong> — User cannot access the data source.</span></span></p></li>
<li><p><span data-ttu-id="a7419-125"><strong>ReadOnly</strong> ユーザーは、データ ソースの読み取りが可能です。</span><span class="sxs-lookup"><span data-stu-id="a7419-125"><strong>ReadOnly</strong> — User can read the data source.</span></span></p></li>
<li><p><span data-ttu-id="a7419-126"><strong>ReadWrite</strong> ユーザーは、データ ソースの読み取り/書き込みが可能です。</span><span class="sxs-lookup"><span data-stu-id="a7419-126"><strong>ReadWrite</strong> — User can read or write to the data source.</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a7419-127">(この効果を使用して、ハンドラーの既定の動作を無効にする) のすべての接続を許可して、[**既定の接続**] セクションでアクセス エントリを設定、削除、または任意の他の\**接続\*\*\*識別子*のセクションをコメントにする場合。</span><span class="sxs-lookup"><span data-stu-id="a7419-127">If you want to allow any connection (in effect, disabling the default handler behavior), set the access entry in the **connect default** section to , and delete or comment out any other **connect** *identifier* section.</span></span>

