---
title: SynchronizeTypeEnum 列挙 (DAO)
TOCTitle: SynchronizeTypeEnum Enumeration
ms:assetid: f9546171-283d-e9bd-5178-41bd4f41c9a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837004(v=office.15)
ms:contentKeyID: 48548812
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: acd4ca20e9b6e17f28a17b012bb182060471e949
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308450"
---
# <a name="synchronizetypeenum-enumeration-dao"></a><span data-ttu-id="84d90-102">SynchronizeTypeEnum 列挙 (DAO)</span><span class="sxs-lookup"><span data-stu-id="84d90-102">SynchronizeTypeEnum enumeration (DAO)</span></span>


<span data-ttu-id="84d90-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="84d90-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="84d90-104">**Synchronize** メソッドで、2 つのレプリカに適用する同期の種類を特定するために使用します。</span><span class="sxs-lookup"><span data-stu-id="84d90-104">Used with the **Synchronize** method to determine the type of synchronization to apply to two replicas.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="84d90-105">名前</span><span class="sxs-lookup"><span data-stu-id="84d90-105">Name</span></span></p></th>
<th><p><span data-ttu-id="84d90-106">値</span><span class="sxs-lookup"><span data-stu-id="84d90-106">Value</span></span></p></th>
<th><p><span data-ttu-id="84d90-107">説明</span><span class="sxs-lookup"><span data-stu-id="84d90-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="84d90-108">dbRepExportChanges</span><span class="sxs-lookup"><span data-stu-id="84d90-108">dbRepExportChanges</span></span></p></td>
<td><p><span data-ttu-id="84d90-109">1-d</span><span class="sxs-lookup"><span data-stu-id="84d90-109">1</span></span></p></td>
<td><p><span data-ttu-id="84d90-110">カレント データベースから対象のデータベースに変更を送信します。</span><span class="sxs-lookup"><span data-stu-id="84d90-110">Sends changes from current database to target database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84d90-111">dbRepImpExpChanges</span><span class="sxs-lookup"><span data-stu-id="84d90-111">dbRepImpExpChanges</span></span></p></td>
<td><p><span data-ttu-id="84d90-112">2/4</span><span class="sxs-lookup"><span data-stu-id="84d90-112">4</span></span></p></td>
<td><p><span data-ttu-id="84d90-113">双方向交換でデータを送受信します。</span><span class="sxs-lookup"><span data-stu-id="84d90-113">Sends and receives data in a bidirectional exchange.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84d90-114">dbRepImportChanges</span><span class="sxs-lookup"><span data-stu-id="84d90-114">dbRepImportChanges</span></span></p></td>
<td><p><span data-ttu-id="84d90-115">pbm-2</span><span class="sxs-lookup"><span data-stu-id="84d90-115">2</span></span></p></td>
<td><p><span data-ttu-id="84d90-116">対象のデータベースから変更を受信します。</span><span class="sxs-lookup"><span data-stu-id="84d90-116">Receives changes from target database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84d90-117">dbRepSyncInternet</span><span class="sxs-lookup"><span data-stu-id="84d90-117">dbRepSyncInternet</span></span></p></td>
<td><p><span data-ttu-id="84d90-118">16</span><span class="sxs-lookup"><span data-stu-id="84d90-118">16</span></span></p></td>
<td><p><span data-ttu-id="84d90-119">双方向交換でデータを送受信します。</span><span class="sxs-lookup"><span data-stu-id="84d90-119">Sends and receives data in a bidirectional exchange.</span></span></p></td>
</tr>
</tbody>
</table>

