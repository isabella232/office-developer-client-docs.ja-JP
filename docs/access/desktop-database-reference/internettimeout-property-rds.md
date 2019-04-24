---
title: internettimeout プロパティ (RDS)
TOCTitle: InternetTimeout property (RDS)
ms:assetid: 66fc6e87-3d23-ce2c-18f5-0fc83ac43801
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249401(v=office.15)
ms:contentKeyID: 48545353
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8c0650a287e2aebc13b89572db112b8f9b333dc6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291242"
---
# <a name="internettimeout-property-rds"></a><span data-ttu-id="1fee2-102">internettimeout プロパティ (RDS)</span><span class="sxs-lookup"><span data-stu-id="1fee2-102">InternetTimeout property (RDS)</span></span>


<span data-ttu-id="1fee2-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="1fee2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1fee2-104">要求がタイムアウトするまでの待機時間をミリ秒単位で示します。</span><span class="sxs-lookup"><span data-stu-id="1fee2-104">Indicates the number of milliseconds to wait before a request times out.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="1fee2-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="1fee2-105">Settings and return values</span></span>

<span data-ttu-id="1fee2-106">要求がタイムアウトするまでのミリ秒数単位の時間を表す長整数型 (**Long**) の値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="1fee2-106">Sets or returns a **Long** value that represents the number of milliseconds before a request will time out.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fee2-107">注釈</span><span class="sxs-lookup"><span data-stu-id="1fee2-107">Remarks</span></span>

<span data-ttu-id="1fee2-108">このプロパティは、HTTP プロトコルまたは HTTPS プロトコルで送信された要求にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="1fee2-108">This property applies only to requests sent with the HTTP or HTTPS protocols.</span></span>

<span data-ttu-id="1fee2-p101">3 層環境での要求の場合、実行が終了するまでに数分間かかることがあります。このプロパティを使って、長時間かかる要求に対する待機時間を指定します。</span><span class="sxs-lookup"><span data-stu-id="1fee2-p101">Requests in a three-tier environment can take several minutes to execute. Use this property to specify additional time for long-running requests.</span></span>

