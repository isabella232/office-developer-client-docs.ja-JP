---
title: VisibleValue プロパティ (DAO)
TOCTitle: VisibleValue Property
ms:assetid: 1e023a1a-fd49-7570-42bd-2f4c06ac5e5e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845809(v=office.15)
ms:contentKeyID: 48543611
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101184
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 0161ea66068457b53a9667a6739c3a3a0458c8c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292616"
---
# <a name="field2visiblevalue-property-dao"></a><span data-ttu-id="9ac39-102">VisibleValue プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="9ac39-102">Field2.VisibleValue property (DAO)</span></span>


<span data-ttu-id="9ac39-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="9ac39-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="9ac39-104">構文</span><span class="sxs-lookup"><span data-stu-id="9ac39-104">Syntax</span></span>

<span data-ttu-id="9ac39-105">*式*。VisibleValue</span><span class="sxs-lookup"><span data-stu-id="9ac39-105">*expression* .VisibleValue</span></span>

<span data-ttu-id="9ac39-106">\*式\***Field2**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="9ac39-106">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ac39-107">注釈</span><span class="sxs-lookup"><span data-stu-id="9ac39-107">Remarks</span></span>

<span data-ttu-id="9ac39-p101">このプロパティには、サーバーのデータベース内に現在あるフィールドの値が含まれます。共有的バッチ更新を実行しているとき、最初のクライアントがデータを取得してからそれを更新するまでの間に、2 番目のクライアントが同じフィールドおよびレコードを変更すると、競合が発生することがあります。競合が発生した場合、このプロパティを使用すると 2 番目のクライアントが設定した値にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="9ac39-p101">This property contains the value of the field that is currently in the database on the server. During an optimistic batch update, a collision may occur where a second client modified the same field and record in between the time the first client retrieved the data and the first client's update attempt. When this happens, the value that the second client set will be accessible through this property.</span></span>

