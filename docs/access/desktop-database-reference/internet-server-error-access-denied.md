---
title: 'インターネット サーバー エラー: アクセスが拒否されました'
TOCTitle: 'Internet Server Error: Access Denied'
ms:assetid: 65f4608b-afec-2867-dae3-e29bae03a6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249395(v=office.15)
ms:contentKeyID: 48545334
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 885bdc14e5d5d346a17e018a509acf5b6c52108d
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944880"
---
# <a name="internet-server-error-access-denied"></a><span data-ttu-id="c9dcc-102">インターネット サーバー エラー: アクセスが拒否されました</span><span class="sxs-lookup"><span data-stu-id="c9dcc-102">Internet Server error: Access Denied</span></span>


<span data-ttu-id="c9dcc-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="c9dcc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c9dcc-104">このエラーが発生した場合は、通常、Microsoft インターネット インフォメーション サービス (IIS) が次の状態を返したことを意味します。</span><span class="sxs-lookup"><span data-stu-id="c9dcc-104">If you get this error, it usually means that Microsoft Internet Information Services (IIS) returned the following status:</span></span>

<span data-ttu-id="c9dcc-105">HTTP\_ステータス\_401 は拒否されました</span><span class="sxs-lookup"><span data-stu-id="c9dcc-105">HTTP\_STATUS\_DENIED 401</span></span>

<span data-ttu-id="c9dcc-106">IIS がアクセスしているディレクトリが適切なアクセス許可を持っているかどうかを確認してください。</span><span class="sxs-lookup"><span data-stu-id="c9dcc-106">Make sure the directories accessed by IIS have proper permissions.</span></span> <span data-ttu-id="c9dcc-107">RDS は、次の 3 つのパスワード認証モードのいずれかで実行されている IIS web サーバーと通信できます。 匿名、基本、または NT チャレンジ/レスポンス (Windows 2000 では統合 Windows 認証と呼ばれます)。</span><span class="sxs-lookup"><span data-stu-id="c9dcc-107">RDS can communicate with an IIS web server running in any one of the three Password Authentication modes: Anonymous, Basic, or NT Challenge/Response (called Integrated Windows authentication in Windows 2000).</span></span> <span data-ttu-id="c9dcc-108">Web サーバーは、Windows NT または Windows 2000 コンピューターである場合、データの送信元のコンピューターへのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="c9dcc-108">Also, the web server must have permissions to the data source computer if it is a Windows NT/Windows 2000 computer.</span></span>

