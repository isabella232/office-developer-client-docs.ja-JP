---
title: Field.VisibleValue プロパティ (DAO)
TOCTitle: VisibleValue Property
ms:assetid: e40fcb43-9a1d-69e7-1544-8f15ef21daf4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835776(v=office.15)
ms:contentKeyID: 48548332
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 892c7b41a692f353ee7e5bdd2191f6e21b8b4cf2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476968"
---
# <a name="fieldvisiblevalue-property-dao"></a><span data-ttu-id="34a6c-102">Field.VisibleValue プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="34a6c-102">Field.VisibleValue Property (DAO)</span></span>


<span data-ttu-id="34a6c-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="34a6c-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="34a6c-104">構文</span><span class="sxs-lookup"><span data-stu-id="34a6c-104">Syntax</span></span>

<span data-ttu-id="34a6c-105">*式*です。VisibleValue</span><span class="sxs-lookup"><span data-stu-id="34a6c-105">*expression* .VisibleValue</span></span>

<span data-ttu-id="34a6c-106">\*式\***Field**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="34a6c-106">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="34a6c-107">注釈</span><span class="sxs-lookup"><span data-stu-id="34a6c-107">Remarks</span></span>

<span data-ttu-id="34a6c-p101">このプロパティは、サーバーのデータベースに現在存在しているフィールドの値を格納します。共有的バッチ更新中、最初のクライアントがデータを取得してから更新を試行するまでの間に、2 番目のクライアントが同じフィールドとレコードを変更すると、競合が発生する可能性があります。この場合、2 番目のクライアントが設定した値にこのプロパティからアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="34a6c-p101">This property contains the value of the field that is currently in the database on the server. During an optimistic batch update, a collision may occur where a second client modified the same field and record in between the time the first client retrieved the data and the first client's update attempt. When this happens, the value that the second client set will be accessible through this property.</span></span>

