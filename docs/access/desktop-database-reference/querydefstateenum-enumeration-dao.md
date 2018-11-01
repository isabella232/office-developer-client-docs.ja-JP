---
title: QueryDefStateEnum 列挙 (DAO)
TOCTitle: QueryDefStateEnum Enumeration
ms:assetid: edfa3085-f8b4-b813-0828-2ba2a9dc0b9d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836359(v=office.15)
ms:contentKeyID: 48548549
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b368079aeb668c9ae72e3955f55159ab2c72a53e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882568"
---
# <a name="querydefstateenum-enumeration-dao"></a><span data-ttu-id="24ca5-102">QueryDefStateEnum 列挙 (DAO)</span><span class="sxs-lookup"><span data-stu-id="24ca5-102">QueryDefStateEnum Enumeration (DAO)</span></span>


<span data-ttu-id="24ca5-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="24ca5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="24ca5-104">**Prepare** プロパティで、クエリの準備方法の指定に使用されるメソッドを指定するために使用します。</span><span class="sxs-lookup"><span data-stu-id="24ca5-104">Used with the **Prepare** property to specify the method used to specify how a query should be prepared.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="24ca5-105">名前</span><span class="sxs-lookup"><span data-stu-id="24ca5-105">Name</span></span></p></th>
<th><p><span data-ttu-id="24ca5-106">値</span><span class="sxs-lookup"><span data-stu-id="24ca5-106">Value</span></span></p></th>
<th><p><span data-ttu-id="24ca5-107">説明</span><span class="sxs-lookup"><span data-stu-id="24ca5-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="24ca5-108">dbQPrepare</span><span class="sxs-lookup"><span data-stu-id="24ca5-108">dbQPrepare</span></span></p></td>
<td><p><span data-ttu-id="24ca5-109">1</span><span class="sxs-lookup"><span data-stu-id="24ca5-109">1</span></span></p></td>
<td><p><span data-ttu-id="24ca5-110">(既定値) ステートメントが準備されます (つまり、ODBC SQLPrepare API が呼び出されます)。</span><span class="sxs-lookup"><span data-stu-id="24ca5-110">(Default) The statement is prepared (that is, the ODBC SQLPrepare API is called).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24ca5-111">dbQUnprepare</span><span class="sxs-lookup"><span data-stu-id="24ca5-111">dbQUnprepare</span></span></p></td>
<td><p><span data-ttu-id="24ca5-112">2</span><span class="sxs-lookup"><span data-stu-id="24ca5-112">2</span></span></p></td>
<td><p><span data-ttu-id="24ca5-113">ステートメントが準備されません (つまり、ODBC SQLExecDirect API が呼び出されます)。</span><span class="sxs-lookup"><span data-stu-id="24ca5-113">The statement is not prepared (that is, the ODBC SQLExecDirect API is called).</span></span></p></td>
</tr>
</tbody>
</table>

