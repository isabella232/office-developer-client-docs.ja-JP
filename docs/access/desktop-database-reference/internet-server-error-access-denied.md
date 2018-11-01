---
title: 'インターネット サーバー エラー: アクセスは拒否されました'
TOCTitle: 'Internet Server Error: Access Denied'
ms:assetid: 65f4608b-afec-2867-dae3-e29bae03a6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249395(v=office.15)
ms:contentKeyID: 48545334
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 132ecc75c01cdc54eb2d7664227b7abb1578cc2f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876541"
---
# <a name="internet-server-error-access-denied"></a><span data-ttu-id="5fc5b-102">インターネット サーバー エラー: アクセスが拒否されました</span><span class="sxs-lookup"><span data-stu-id="5fc5b-102">Internet Server Error: Access Denied</span></span>


<span data-ttu-id="5fc5b-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="5fc5b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5fc5b-104">このエラーが発生した場合は、通常、Microsoft インターネット インフォメーション サービス (IIS) が次の状態を返したことを意味します。</span><span class="sxs-lookup"><span data-stu-id="5fc5b-104">If you get this error, it usually means that Microsoft Internet Information Services (IIS) returned the following status:</span></span>

<span data-ttu-id="5fc5b-105">HTTP\_ステータス\_401 は拒否されました</span><span class="sxs-lookup"><span data-stu-id="5fc5b-105">HTTP\_STATUS\_DENIED 401</span></span>

<span data-ttu-id="5fc5b-106">IIS がアクセスしているディレクトリが適切なアクセス許可を持っているかどうかを確認してください。</span><span class="sxs-lookup"><span data-stu-id="5fc5b-106">Make sure the directories accessed by IIS have proper permissions.</span></span> <span data-ttu-id="5fc5b-107">RDS は、次の 3 つのパスワード認証モードのいずれかで実行されている IIS web サーバーと通信できます。 匿名、基本、または NT チャレンジ/レスポンス (Windows 2000 では統合 Windows 認証と呼ばれます)。</span><span class="sxs-lookup"><span data-stu-id="5fc5b-107">RDS can communicate with an IIS web server running in any one of the three Password Authentication modes: Anonymous, Basic, or NT Challenge/Response (called Integrated Windows authentication in Windows 2000).</span></span> <span data-ttu-id="5fc5b-108">Web サーバーは、Windows NT または Windows 2000 コンピューターである場合、データの送信元のコンピューターへのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="5fc5b-108">Also, the web server must have permissions to the data source computer if it is a Windows NT/Windows 2000 computer.</span></span>

