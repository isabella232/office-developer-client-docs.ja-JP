---
title: CursorDriverEnum 列挙 (DAO)
TOCTitle: CursorDriverEnum Enumeration
ms:assetid: d0312ece-c30a-7d61-d5f3-75edf0d0afc8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834707(v=office.15)
ms:contentKeyID: 48547832
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bcce8eefad7fcad7dee7e46274ffc45125dc36c9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478566"
---
# <a name="cursordriverenum-enumeration-dao"></a><span data-ttu-id="5b4b5-102">CursorDriverEnum 列挙 (DAO)</span><span class="sxs-lookup"><span data-stu-id="5b4b5-102">CursorDriverEnum Enumeration (DAO)</span></span>


<span data-ttu-id="5b4b5-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="5b4b5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5b4b5-104">カーソル ドライバーの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="5b4b5-104">Specifies the type of cursor driver.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5b4b5-105">名前</span><span class="sxs-lookup"><span data-stu-id="5b4b5-105">Name</span></span></p></th>
<th><p><span data-ttu-id="5b4b5-106">値</span><span class="sxs-lookup"><span data-stu-id="5b4b5-106">Value</span></span></p></th>
<th><p><span data-ttu-id="5b4b5-107">説明</span><span class="sxs-lookup"><span data-stu-id="5b4b5-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5b4b5-108">dbUseClientBatchCursor</span><span class="sxs-lookup"><span data-stu-id="5b4b5-108">dbUseClientBatchCursor</span></span></p></td>
<td><p><span data-ttu-id="5b4b5-109">3</span><span class="sxs-lookup"><span data-stu-id="5b4b5-109">3</span></span></p></td>
<td><p><span data-ttu-id="5b4b5-p101">常に FoxPro カーソル ライブラリを使用します。一括更新を実行する場合には、このオプションを必ず指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5b4b5-p101">Always uses the FoxPro Cursor Library. This option is required for performing batch updates.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b4b5-112">dbUseDefaultCursor</span><span class="sxs-lookup"><span data-stu-id="5b4b5-112">dbUseDefaultCursor</span></span></p></td>
<td><p><span data-ttu-id="5b4b5-113">-1</span><span class="sxs-lookup"><span data-stu-id="5b4b5-113">-1</span></span></p></td>
<td><p><span data-ttu-id="5b4b5-114">(既定値) サーバーがサーバー側カーソルをサポートする場合は、サーバー側カーソルを使用します。それ以外の場合は、ODBC カーソル ライブラリを使用します。</span><span class="sxs-lookup"><span data-stu-id="5b4b5-114">(Default) Uses server-side cursors if the server supports them; otherwise uses the ODBC Cursor Library.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5b4b5-115">dbUseNoCursor</span><span class="sxs-lookup"><span data-stu-id="5b4b5-115">dbUseNoCursor</span></span></p></td>
<td><p><span data-ttu-id="5b4b5-116">4</span><span class="sxs-lookup"><span data-stu-id="5b4b5-116">4</span></span></p></td>
<td><p><span data-ttu-id="5b4b5-117">付けて順方向専用、読み取り専用、行セット サイズが 1 のすべてのカーソル (つまり、<strong>レコード セット</strong>オブジェクト) を開きます。</span><span class="sxs-lookup"><span data-stu-id="5b4b5-117">Opens all cursors (that is, <strong>Recordset</strong> objects) as forward-only type, read-only, with a rowset size of 1.</span></span> <span data-ttu-id="5b4b5-118">呼ばれる&quot;カーソルレス クエリします。&quot;</span><span class="sxs-lookup"><span data-stu-id="5b4b5-118">Also known as &quot;cursorless queries.&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b4b5-119">dbUseODBCCursor</span><span class="sxs-lookup"><span data-stu-id="5b4b5-119">dbUseODBCCursor</span></span></p></td>
<td><p><span data-ttu-id="5b4b5-120">1</span><span class="sxs-lookup"><span data-stu-id="5b4b5-120">1</span></span></p></td>
<td><p><span data-ttu-id="5b4b5-p103">常に ODBC カーソル ライブラリを使用します。このオプションは、結果セットが小さい場合にはパフォーマンスが高くなりますが、結果セットが大きくなるとパフォーマンスが急激に低下します。</span><span class="sxs-lookup"><span data-stu-id="5b4b5-p103">Always uses the ODBC Cursor Library. This option provides better performance for small result sets, but degrades quickly for larger result sets.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5b4b5-123">dbUseServerCursor</span><span class="sxs-lookup"><span data-stu-id="5b4b5-123">dbUseServerCursor</span></span></p></td>
<td><p><span data-ttu-id="5b4b5-124">2</span><span class="sxs-lookup"><span data-stu-id="5b4b5-124">2</span></span></p></td>
<td><p><span data-ttu-id="5b4b5-p104">常にサーバー側カーソルを使用します。大規模な操作のほとんどでは、このオプションによって高いパフォーマンスが得られますが、ネットワーク トラフィックが増える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="5b4b5-p104">Always uses server-side cursors. For most large operations this option provides better performance, but might cause more network traffic.</span></span></p></td>
</tr>
</tbody>
</table>

