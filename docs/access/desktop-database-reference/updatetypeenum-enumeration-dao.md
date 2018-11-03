---
title: UpdateTypeEnum 列挙 (DAO)
TOCTitle: UpdateTypeEnum Enumeration
ms:assetid: 7ac38bae-27fc-f3d0-5b75-569bce547954
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196186(v=office.15)
ms:contentKeyID: 48545800
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d38cf4554837c9c6434b7607746f2c40836ac950
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944621"
---
# <a name="updatetypeenum-enumeration-dao"></a><span data-ttu-id="1687f-102">UpdateTypeEnum 列挙 (DAO)</span><span class="sxs-lookup"><span data-stu-id="1687f-102">UpdateTypeEnum enumeration (DAO)</span></span>


<span data-ttu-id="1687f-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="1687f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1687f-104">**Update** メソッドで、ディスクに書き込む更新を指定するために使用します。</span><span class="sxs-lookup"><span data-stu-id="1687f-104">Used with the **Update** method to specify which updates to write to disk.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1687f-105">名前</span><span class="sxs-lookup"><span data-stu-id="1687f-105">Name</span></span></p></th>
<th><p><span data-ttu-id="1687f-106">値</span><span class="sxs-lookup"><span data-stu-id="1687f-106">Value</span></span></p></th>
<th><p><span data-ttu-id="1687f-107">説明</span><span class="sxs-lookup"><span data-stu-id="1687f-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1687f-108">dbUpdateBatch</span><span class="sxs-lookup"><span data-stu-id="1687f-108">dbUpdateBatch</span></span></p></td>
<td><p><span data-ttu-id="1687f-109">4</span><span class="sxs-lookup"><span data-stu-id="1687f-109">4</span></span></p></td>
<td><p><span data-ttu-id="1687f-110">更新キャッシュ内の保留中のすべての変更をディスクに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="1687f-110">All pending changes in the update cache are written to disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1687f-111">dbUpdateCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="1687f-111">dbUpdateCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="1687f-112">2</span><span class="sxs-lookup"><span data-stu-id="1687f-112">2</span></span></p></td>
<td><p><span data-ttu-id="1687f-113">現在のレコードの保留中の変更のみをディスクに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="1687f-113">Only the current record's pending changes are written to disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1687f-114">dbUpdateRegular</span><span class="sxs-lookup"><span data-stu-id="1687f-114">dbUpdateRegular</span></span></p></td>
<td><p><span data-ttu-id="1687f-115">1</span><span class="sxs-lookup"><span data-stu-id="1687f-115">1</span></span></p></td>
<td><p><span data-ttu-id="1687f-116">(既定値) 保留中の変更をキャッシュせず、ディスクに直ちに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="1687f-116">(Default) Pending changes are not cached and are written to disk immediately.</span></span></p></td>
</tr>
</tbody>
</table>

