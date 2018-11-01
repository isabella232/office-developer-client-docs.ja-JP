---
title: SynchronizeTypeEnum 列挙 (DAO)
TOCTitle: SynchronizeTypeEnum Enumeration
ms:assetid: f9546171-283d-e9bd-5178-41bd4f41c9a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837004(v=office.15)
ms:contentKeyID: 48548812
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b6b3893f0af259d6cabab0622dd518a77206b93c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868008"
---
# <a name="synchronizetypeenum-enumeration-dao"></a><span data-ttu-id="3106b-102">SynchronizeTypeEnum 列挙 (DAO)</span><span class="sxs-lookup"><span data-stu-id="3106b-102">SynchronizeTypeEnum Enumeration (DAO)</span></span>


<span data-ttu-id="3106b-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="3106b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3106b-104">**Synchronize** メソッドで、2 つのレプリカに適用する同期の種類を特定するために使用します。</span><span class="sxs-lookup"><span data-stu-id="3106b-104">Used with the **Synchronize** method to determine the type of synchronization to apply to two replicas.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3106b-105">名前</span><span class="sxs-lookup"><span data-stu-id="3106b-105">Name</span></span></p></th>
<th><p><span data-ttu-id="3106b-106">値</span><span class="sxs-lookup"><span data-stu-id="3106b-106">Value</span></span></p></th>
<th><p><span data-ttu-id="3106b-107">説明</span><span class="sxs-lookup"><span data-stu-id="3106b-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3106b-108">dbRepExportChanges</span><span class="sxs-lookup"><span data-stu-id="3106b-108">dbRepExportChanges</span></span></p></td>
<td><p><span data-ttu-id="3106b-109">1</span><span class="sxs-lookup"><span data-stu-id="3106b-109">1</span></span></p></td>
<td><p><span data-ttu-id="3106b-110">カレント データベースから対象のデータベースに変更を送信します。</span><span class="sxs-lookup"><span data-stu-id="3106b-110">Sends changes from current database to target database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3106b-111">dbRepImpExpChanges</span><span class="sxs-lookup"><span data-stu-id="3106b-111">dbRepImpExpChanges</span></span></p></td>
<td><p><span data-ttu-id="3106b-112">4</span><span class="sxs-lookup"><span data-stu-id="3106b-112">4</span></span></p></td>
<td><p><span data-ttu-id="3106b-113">双方向交換でデータを送受信します。</span><span class="sxs-lookup"><span data-stu-id="3106b-113">Sends and receives data in a bidirectional exchange.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3106b-114">dbRepImportChanges</span><span class="sxs-lookup"><span data-stu-id="3106b-114">dbRepImportChanges</span></span></p></td>
<td><p><span data-ttu-id="3106b-115">2</span><span class="sxs-lookup"><span data-stu-id="3106b-115">2</span></span></p></td>
<td><p><span data-ttu-id="3106b-116">対象のデータベースから変更を受信します。</span><span class="sxs-lookup"><span data-stu-id="3106b-116">Receives changes from target database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3106b-117">dbRepSyncInternet</span><span class="sxs-lookup"><span data-stu-id="3106b-117">dbRepSyncInternet</span></span></p></td>
<td><p><span data-ttu-id="3106b-118">16</span><span class="sxs-lookup"><span data-stu-id="3106b-118">16</span></span></p></td>
<td><p><span data-ttu-id="3106b-119">双方向交換でデータを送受信します。</span><span class="sxs-lookup"><span data-stu-id="3106b-119">Sends and receives data in a bidirectional exchange.</span></span></p></td>
</tr>
</tbody>
</table>

