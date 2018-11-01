---
title: UpdateTypeEnum 列挙 (DAO)
TOCTitle: UpdateTypeEnum Enumeration
ms:assetid: 7ac38bae-27fc-f3d0-5b75-569bce547954
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196186(v=office.15)
ms:contentKeyID: 48545800
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bd2ef7888f511b3f1577ec5fe60ef0ef7dda614a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873447"
---
# <a name="updatetypeenum-enumeration-dao"></a><span data-ttu-id="d19d0-102">UpdateTypeEnum 列挙 (DAO)</span><span class="sxs-lookup"><span data-stu-id="d19d0-102">UpdateTypeEnum Enumeration (DAO)</span></span>


<span data-ttu-id="d19d0-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="d19d0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d19d0-104">**Update** メソッドで、ディスクに書き込む更新を指定するために使用します。</span><span class="sxs-lookup"><span data-stu-id="d19d0-104">Used with the **Update** method to specify which updates to write to disk.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d19d0-105">名前</span><span class="sxs-lookup"><span data-stu-id="d19d0-105">Name</span></span></p></th>
<th><p><span data-ttu-id="d19d0-106">値</span><span class="sxs-lookup"><span data-stu-id="d19d0-106">Value</span></span></p></th>
<th><p><span data-ttu-id="d19d0-107">説明</span><span class="sxs-lookup"><span data-stu-id="d19d0-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d19d0-108">dbUpdateBatch</span><span class="sxs-lookup"><span data-stu-id="d19d0-108">dbUpdateBatch</span></span></p></td>
<td><p><span data-ttu-id="d19d0-109">4</span><span class="sxs-lookup"><span data-stu-id="d19d0-109">4</span></span></p></td>
<td><p><span data-ttu-id="d19d0-110">更新キャッシュ内の保留中のすべての変更をディスクに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="d19d0-110">All pending changes in the update cache are written to disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d19d0-111">dbUpdateCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="d19d0-111">dbUpdateCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="d19d0-112">2</span><span class="sxs-lookup"><span data-stu-id="d19d0-112">2</span></span></p></td>
<td><p><span data-ttu-id="d19d0-113">現在のレコードの保留中の変更のみをディスクに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="d19d0-113">Only the current record's pending changes are written to disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d19d0-114">dbUpdateRegular</span><span class="sxs-lookup"><span data-stu-id="d19d0-114">dbUpdateRegular</span></span></p></td>
<td><p><span data-ttu-id="d19d0-115">1</span><span class="sxs-lookup"><span data-stu-id="d19d0-115">1</span></span></p></td>
<td><p><span data-ttu-id="d19d0-116">(既定値) 保留中の変更をキャッシュせず、ディスクに直ちに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="d19d0-116">(Default) Pending changes are not cached and are written to disk immediately.</span></span></p></td>
</tr>
</tbody>
</table>

