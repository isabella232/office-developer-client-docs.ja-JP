---
title: UpdateTypeEnum 列挙 (DAO)
TOCTitle: UpdateTypeEnum Enumeration
ms:assetid: 7ac38bae-27fc-f3d0-5b75-569bce547954
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196186(v=office.15)
ms:contentKeyID: 48545800
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4ee8638d6fdade7e6955613964f619270574ce4b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477443"
---
# <a name="updatetypeenum-enumeration-dao"></a><span data-ttu-id="94b31-102">UpdateTypeEnum 列挙 (DAO)</span><span class="sxs-lookup"><span data-stu-id="94b31-102">UpdateTypeEnum Enumeration (DAO)</span></span>


<span data-ttu-id="94b31-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="94b31-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="94b31-104">**Update** メソッドで、ディスクに書き込む更新を指定するために使用します。</span><span class="sxs-lookup"><span data-stu-id="94b31-104">Used with the **Update** method to specify which updates to write to disk.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="94b31-105">名前</span><span class="sxs-lookup"><span data-stu-id="94b31-105">Name</span></span></p></th>
<th><p><span data-ttu-id="94b31-106">値</span><span class="sxs-lookup"><span data-stu-id="94b31-106">Value</span></span></p></th>
<th><p><span data-ttu-id="94b31-107">説明</span><span class="sxs-lookup"><span data-stu-id="94b31-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="94b31-108">dbUpdateBatch</span><span class="sxs-lookup"><span data-stu-id="94b31-108">dbUpdateBatch</span></span></p></td>
<td><p><span data-ttu-id="94b31-109">4</span><span class="sxs-lookup"><span data-stu-id="94b31-109">4</span></span></p></td>
<td><p><span data-ttu-id="94b31-110">更新キャッシュ内の保留中のすべての変更をディスクに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="94b31-110">All pending changes in the update cache are written to disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b31-111">dbUpdateCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="94b31-111">dbUpdateCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="94b31-112">2</span><span class="sxs-lookup"><span data-stu-id="94b31-112">2</span></span></p></td>
<td><p><span data-ttu-id="94b31-113">現在のレコードの保留中の変更のみをディスクに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="94b31-113">Only the current record's pending changes are written to disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b31-114">dbUpdateRegular</span><span class="sxs-lookup"><span data-stu-id="94b31-114">dbUpdateRegular</span></span></p></td>
<td><p><span data-ttu-id="94b31-115">1</span><span class="sxs-lookup"><span data-stu-id="94b31-115">1</span></span></p></td>
<td><p><span data-ttu-id="94b31-116">(既定値) 保留中の変更をキャッシュせず、ディスクに直ちに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="94b31-116">(Default) Pending changes are not cached and are written to disk immediately.</span></span></p></td>
</tr>
</tbody>
</table>

