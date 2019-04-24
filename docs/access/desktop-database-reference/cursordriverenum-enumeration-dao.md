---
title: カーソルの列挙 (DAO)
TOCTitle: CursorDriverEnum enumeration
ms:assetid: d0312ece-c30a-7d61-d5f3-75edf0d0afc8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834707(v=office.15)
ms:contentKeyID: 48547832
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2f2bf52943a84d6f2e60891d63810bc0bbb6ecb3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295248"
---
# <a name="cursordriverenum-enumeration-dao"></a><span data-ttu-id="1a547-102">カーソルの列挙 (DAO)</span><span class="sxs-lookup"><span data-stu-id="1a547-102">CursorDriverEnum enumeration (DAO)</span></span>

<span data-ttu-id="1a547-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="1a547-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1a547-104">カーソル ドライバーの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="1a547-104">Specifies the type of cursor driver.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1a547-105">名前</span><span class="sxs-lookup"><span data-stu-id="1a547-105">Name</span></span></p></th>
<th><p><span data-ttu-id="1a547-106">値</span><span class="sxs-lookup"><span data-stu-id="1a547-106">Value</span></span></p></th>
<th><p><span data-ttu-id="1a547-107">説明</span><span class="sxs-lookup"><span data-stu-id="1a547-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1a547-108">dbUseClientBatchCursor</span><span class="sxs-lookup"><span data-stu-id="1a547-108">dbUseClientBatchCursor</span></span></p></td>
<td><p><span data-ttu-id="1a547-109">1/3</span><span class="sxs-lookup"><span data-stu-id="1a547-109">3</span></span></p></td>
<td><p><span data-ttu-id="1a547-p101">常に FoxPro カーソル ライブラリを使用します。一括更新を実行する場合には、このオプションを必ず指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1a547-p101">Always uses the FoxPro Cursor Library. This option is required for performing batch updates.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a547-112">dbusedefaultcursor</span><span class="sxs-lookup"><span data-stu-id="1a547-112">dbUseDefaultCursor</span></span></p></td>
<td><p><span data-ttu-id="1a547-113">-1</span><span class="sxs-lookup"><span data-stu-id="1a547-113">-1</span></span></p></td>
<td><p><span data-ttu-id="1a547-114">(既定値) サーバーがサーバー側カーソルをサポートする場合は、サーバー側カーソルを使用します。それ以外の場合は、ODBC カーソル ライブラリを使用します。</span><span class="sxs-lookup"><span data-stu-id="1a547-114">(Default) Uses server-side cursors if the server supports them; otherwise uses the ODBC Cursor Library.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a547-115">dbUseNoCursor</span><span class="sxs-lookup"><span data-stu-id="1a547-115">dbUseNoCursor</span></span></p></td>
<td><p><span data-ttu-id="1a547-116">2/4</span><span class="sxs-lookup"><span data-stu-id="1a547-116">4</span></span></p></td>
<td><p><span data-ttu-id="1a547-117">すべてのカーソル (つまり <strong>Recordset</strong> オブジェクト) を、行セットのサイズが 1 である前方のみの読み取り専用カーソルとして開きます。</span><span class="sxs-lookup"><span data-stu-id="1a547-117">Opens all cursors (that is, <strong>Recordset</strong> objects) as forward-only type, read-only, with a rowset size of 1.</span></span> <span data-ttu-id="1a547-118">カーソルの少ない&quot;クエリとも呼ばれます。&quot;</span><span class="sxs-lookup"><span data-stu-id="1a547-118">Also known as &quot;cursorless queries.&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a547-119">dbUseODBCCursor</span><span class="sxs-lookup"><span data-stu-id="1a547-119">dbUseODBCCursor</span></span></p></td>
<td><p><span data-ttu-id="1a547-120">1-d</span><span class="sxs-lookup"><span data-stu-id="1a547-120">1</span></span></p></td>
<td><p><span data-ttu-id="1a547-p103">常に ODBC カーソル ライブラリを使用します。このオプションは、結果セットが小さい場合にはパフォーマンスが高くなりますが、結果セットが大きくなるとパフォーマンスが急激に低下します。</span><span class="sxs-lookup"><span data-stu-id="1a547-p103">Always uses the ODBC Cursor Library. This option provides better performance for small result sets, but degrades quickly for larger result sets.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a547-123">dbuseservercursor</span><span class="sxs-lookup"><span data-stu-id="1a547-123">dbUseServerCursor</span></span></p></td>
<td><p><span data-ttu-id="1a547-124">pbm-2</span><span class="sxs-lookup"><span data-stu-id="1a547-124">2</span></span></p></td>
<td><p><span data-ttu-id="1a547-p104">常にサーバー側カーソルを使用します。大規模な操作のほとんどでは、このオプションによって高いパフォーマンスが得られますが、ネットワーク トラフィックが増える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="1a547-p104">Always uses server-side cursors. For most large operations this option provides better performance, but might cause more network traffic.</span></span></p></td>
</tr>
</tbody>
</table>

