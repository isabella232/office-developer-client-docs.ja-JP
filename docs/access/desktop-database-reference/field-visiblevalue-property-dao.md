---
title: Field.VisibleValue プロパティ (DAO)
TOCTitle: VisibleValue Property
ms:assetid: e40fcb43-9a1d-69e7-1544-8f15ef21daf4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835776(v=office.15)
ms:contentKeyID: 48548332
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1b3e1b6ec6cd34112f0ba1d84101390bbd400f82
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712457"
---
# <a name="fieldvisiblevalue-property-dao"></a><span data-ttu-id="1fc04-102">Field.VisibleValue プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="1fc04-102">Field.VisibleValue property (DAO)</span></span>


<span data-ttu-id="1fc04-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="1fc04-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="1fc04-104">構文</span><span class="sxs-lookup"><span data-stu-id="1fc04-104">Syntax</span></span>

<span data-ttu-id="1fc04-105">*式*です。VisibleValue</span><span class="sxs-lookup"><span data-stu-id="1fc04-105">*expression* .VisibleValue</span></span>

<span data-ttu-id="1fc04-106">\*式\***Field**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="1fc04-106">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fc04-107">注釈</span><span class="sxs-lookup"><span data-stu-id="1fc04-107">Remarks</span></span>

<span data-ttu-id="1fc04-p101">このプロパティは、サーバーのデータベースに現在存在しているフィールドの値を格納します。共有的バッチ更新中、最初のクライアントがデータを取得してから更新を試行するまでの間に、2 番目のクライアントが同じフィールドとレコードを変更すると、競合が発生する可能性があります。この場合、2 番目のクライアントが設定した値にこのプロパティからアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="1fc04-p101">This property contains the value of the field that is currently in the database on the server. During an optimistic batch update, a collision may occur where a second client modified the same field and record in between the time the first client retrieved the data and the first client's update attempt. When this happens, the value that the second client set will be accessible through this property.</span></span>

