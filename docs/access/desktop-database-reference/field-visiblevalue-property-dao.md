---
title: VisibleValue プロパティ (DAO)
TOCTitle: VisibleValue Property
ms:assetid: e40fcb43-9a1d-69e7-1544-8f15ef21daf4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835776(v=office.15)
ms:contentKeyID: 48548332
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1b3e1b6ec6cd34112f0ba1d84101390bbd400f82
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292917"
---
# <a name="fieldvisiblevalue-property-dao"></a><span data-ttu-id="9d245-102">VisibleValue プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="9d245-102">Field.VisibleValue property (DAO)</span></span>


<span data-ttu-id="9d245-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="9d245-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="9d245-104">構文</span><span class="sxs-lookup"><span data-stu-id="9d245-104">Syntax</span></span>

<span data-ttu-id="9d245-105">*式*。VisibleValue</span><span class="sxs-lookup"><span data-stu-id="9d245-105">*expression* .VisibleValue</span></span>

<span data-ttu-id="9d245-106">\*式\***Field**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="9d245-106">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d245-107">注釈</span><span class="sxs-lookup"><span data-stu-id="9d245-107">Remarks</span></span>

<span data-ttu-id="9d245-p101">このプロパティには、サーバーのデータベース内に現在あるフィールドの値が含まれます。共有的バッチ更新を実行しているとき、最初のクライアントがデータを取得してからそれを更新するまでの間に、2 番目のクライアントが同じフィールドおよびレコードを変更すると、競合が発生することがあります。競合が発生した場合、このプロパティを使用すると 2 番目のクライアントが設定した値にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="9d245-p101">This property contains the value of the field that is currently in the database on the server. During an optimistic batch update, a collision may occur where a second client modified the same field and record in between the time the first client retrieved the data and the first client's update attempt. When this happens, the value that the second client set will be accessible through this property.</span></span>

