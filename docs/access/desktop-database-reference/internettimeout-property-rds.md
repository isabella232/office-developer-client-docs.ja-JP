---
title: InternetTimeout プロパティ (RDS)
TOCTitle: InternetTimeout Property (RDS)
ms:assetid: 66fc6e87-3d23-ce2c-18f5-0fc83ac43801
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249401(v=office.15)
ms:contentKeyID: 48545353
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 929b166a308276836fbe4a48a2461ef7eb0caba2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476225"
---
# <a name="internettimeout-property-rds"></a><span data-ttu-id="4c414-102">InternetTimeout プロパティ (RDS)</span><span class="sxs-lookup"><span data-stu-id="4c414-102">InternetTimeout Property (RDS)</span></span>


<span data-ttu-id="4c414-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="4c414-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="4c414-104">要求がタイムアウトするまでの待機時間をミリ秒単位で示します。</span><span class="sxs-lookup"><span data-stu-id="4c414-104">Indicates the number of milliseconds to wait before a request times out.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="4c414-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="4c414-105">Settings and Return Values</span></span>

<span data-ttu-id="4c414-106">要求がタイムアウトするまでのミリ秒数単位の時間を表す長整数型 ( **Long** ) の値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="4c414-106">Sets or returns a **Long** value that represents the number of milliseconds before a request will time out.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c414-107">解説</span><span class="sxs-lookup"><span data-stu-id="4c414-107">Remarks</span></span>

<span data-ttu-id="4c414-108">このプロパティは、HTTP プロトコルまたは HTTPS プロトコルで送信された要求にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="4c414-108">This property applies only to requests sent with the HTTP or HTTPS protocols.</span></span>

<span data-ttu-id="4c414-p101">3 層環境での要求の場合、実行が終了するまでに数分間かかることがあります。このプロパティを使って、長時間かかる要求に対する待機時間を指定します。</span><span class="sxs-lookup"><span data-stu-id="4c414-p101">Requests in a three-tier environment can take several minutes to execute. Use this property to specify additional time for long-running requests.</span></span>

