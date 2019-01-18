---
title: 'インターネット サーバー エラー: アクセスが拒否されました'
TOCTitle: 'Internet Server Error: Access Denied'
ms:assetid: 65f4608b-afec-2867-dae3-e29bae03a6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249395(v=office.15)
ms:contentKeyID: 48545334
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: af823f46653b3ec83950c2e2cfe639b514196b08
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720388"
---
# <a name="internet-server-error-access-denied"></a><span data-ttu-id="171ca-102">インターネット サーバー エラー: アクセスが拒否されました</span><span class="sxs-lookup"><span data-stu-id="171ca-102">Internet Server error: Access Denied</span></span>


<span data-ttu-id="171ca-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="171ca-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="171ca-104">このエラーが発生した場合は、通常、Microsoft インターネット インフォメーション サービス (IIS) が次の状態を返したことを意味します。</span><span class="sxs-lookup"><span data-stu-id="171ca-104">If you get this error, it usually means that Microsoft Internet Information Services (IIS) returned the following status:</span></span>

<span data-ttu-id="171ca-105">HTTP\_ステータス\_401 は拒否されました</span><span class="sxs-lookup"><span data-stu-id="171ca-105">HTTP\_STATUS\_DENIED 401</span></span>

<span data-ttu-id="171ca-106">IIS がアクセスしているディレクトリが適切なアクセス許可を持っているかどうかを確認してください。</span><span class="sxs-lookup"><span data-stu-id="171ca-106">Make sure the directories accessed by IIS have proper permissions.</span></span> <span data-ttu-id="171ca-107">RDS は、次の 3 つのパスワード認証モードのいずれかで実行されている IIS web サーバーと通信できます。 匿名、基本、または NT チャレンジ/レスポンス (Windows 2000 では統合 Windows 認証と呼ばれます)。</span><span class="sxs-lookup"><span data-stu-id="171ca-107">RDS can communicate with an IIS web server running in any one of the three Password Authentication modes: Anonymous, Basic, or NT Challenge/Response (called Integrated Windows authentication in Windows 2000).</span></span> <span data-ttu-id="171ca-108">Web サーバーは、Windows NT または Windows 2000 コンピューターである場合、データの送信元のコンピューターへのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="171ca-108">Also, the web server must have permissions to the data source computer if it is a Windows NT/Windows 2000 computer.</span></span>

