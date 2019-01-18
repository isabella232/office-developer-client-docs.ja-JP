---
title: 可能 (DAO) の列挙
TOCTitle: QueryDefStateEnum Enumeration
ms:assetid: edfa3085-f8b4-b813-0828-2ba2a9dc0b9d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836359(v=office.15)
ms:contentKeyID: 48548549
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0ca9923b1604b17c1d7f64d2d968378fec4a8c24
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698660"
---
# <a name="querydefstateenum-enumeration-dao"></a><span data-ttu-id="96cb8-102">可能 (DAO) の列挙</span><span class="sxs-lookup"><span data-stu-id="96cb8-102">QueryDefStateEnum enumeration (DAO)</span></span>


<span data-ttu-id="96cb8-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="96cb8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="96cb8-104">**Prepare** プロパティで、クエリの準備方法の指定に使用されるメソッドを指定するために使用します。</span><span class="sxs-lookup"><span data-stu-id="96cb8-104">Used with the **Prepare** property to specify the method used to specify how a query should be prepared.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="96cb8-105">名前</span><span class="sxs-lookup"><span data-stu-id="96cb8-105">Name</span></span></p></th>
<th><p><span data-ttu-id="96cb8-106">値</span><span class="sxs-lookup"><span data-stu-id="96cb8-106">Value</span></span></p></th>
<th><p><span data-ttu-id="96cb8-107">説明</span><span class="sxs-lookup"><span data-stu-id="96cb8-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="96cb8-108">dbQPrepare</span><span class="sxs-lookup"><span data-stu-id="96cb8-108">dbQPrepare</span></span></p></td>
<td><p><span data-ttu-id="96cb8-109">1</span><span class="sxs-lookup"><span data-stu-id="96cb8-109">1</span></span></p></td>
<td><p><span data-ttu-id="96cb8-110">(既定値) ステートメントが準備されます (つまり、ODBC SQLPrepare API が呼び出されます)。</span><span class="sxs-lookup"><span data-stu-id="96cb8-110">(Default) The statement is prepared (that is, the ODBC SQLPrepare API is called).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96cb8-111">dbQUnprepare</span><span class="sxs-lookup"><span data-stu-id="96cb8-111">dbQUnprepare</span></span></p></td>
<td><p><span data-ttu-id="96cb8-112">2</span><span class="sxs-lookup"><span data-stu-id="96cb8-112">2</span></span></p></td>
<td><p><span data-ttu-id="96cb8-113">ステートメントが準備されません (つまり、ODBC SQLExecDirect API が呼び出されます)。</span><span class="sxs-lookup"><span data-stu-id="96cb8-113">The statement is not prepared (that is, the ODBC SQLExecDirect API is called).</span></span></p></td>
</tr>
</tbody>
</table>

