---
title: Field2.VisibleValue プロパティ (DAO)
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
ms.openlocfilehash: 896cc3866b52aeb8bbd2956ea84f9470671a407a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873258"
---
# <a name="field2visiblevalue-property-dao"></a><span data-ttu-id="67347-102">Field2.VisibleValue プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="67347-102">Field2.VisibleValue Property (DAO)</span></span>


<span data-ttu-id="67347-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="67347-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="67347-104">構文</span><span class="sxs-lookup"><span data-stu-id="67347-104">Syntax</span></span>

<span data-ttu-id="67347-105">*式*です。VisibleValue</span><span class="sxs-lookup"><span data-stu-id="67347-105">*expression* .VisibleValue</span></span>

<span data-ttu-id="67347-106">\*式\***Field2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="67347-106">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="67347-107">注釈</span><span class="sxs-lookup"><span data-stu-id="67347-107">Remarks</span></span>

<span data-ttu-id="67347-p101">このプロパティは、サーバーのデータベースに現在存在しているフィールドの値を格納します。共有的バッチ更新中、最初のクライアントがデータを取得してから更新を試行するまでの間に、2 番目のクライアントが同じフィールドとレコードを変更すると、競合が発生する可能性があります。この場合、2 番目のクライアントが設定した値にこのプロパティからアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="67347-p101">This property contains the value of the field that is currently in the database on the server. During an optimistic batch update, a collision may occur where a second client modified the same field and record in between the time the first client retrieved the data and the first client's update attempt. When this happens, the value that the second client set will be accessible through this property.</span></span>

