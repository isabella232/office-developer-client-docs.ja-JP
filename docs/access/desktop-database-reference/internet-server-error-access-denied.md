---
title: 'インターネット サーバー エラー: アクセスは拒否されました'
TOCTitle: 'Internet Server Error: Access Denied'
ms:assetid: 65f4608b-afec-2867-dae3-e29bae03a6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249395(v=office.15)
ms:contentKeyID: 48545334
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: db78b6f2c51e2e5df918622043e33abc6bc9e674
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477451"
---
# <a name="internet-server-error-access-denied"></a><span data-ttu-id="0dbe5-102">インターネット サーバー エラー: アクセスは拒否されました</span><span class="sxs-lookup"><span data-stu-id="0dbe5-102">Internet Server Error: Access Denied</span></span>


<span data-ttu-id="0dbe5-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="0dbe5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0dbe5-104">このエラーが発生した場合は、通常、Microsoft インターネット インフォメーション サービス (IIS) が次の状態を返したことを意味します。</span><span class="sxs-lookup"><span data-stu-id="0dbe5-104">If you get this error, it usually means that Microsoft Internet Information Services (IIS) returned the following status:</span></span>

<span data-ttu-id="0dbe5-105">HTTP\_ステータス\_401 は拒否されました</span><span class="sxs-lookup"><span data-stu-id="0dbe5-105">HTTP\_STATUS\_DENIED 401</span></span>

<span data-ttu-id="0dbe5-p101">IIS がアクセスしているディレクトリが適切なアクセス許可を持っているかどうかを確認してください。RDS は、匿名、基本、または NT チャレンジ/レスポンス (Windows 2000 では統合 Windows 認証) の 3 種類のパスワード認証モードで実行している IIS Web サーバーと通信できます。また、データ ソース コンピューターが Windows NT/Windows 2000 コンピューターの場合、Web サーバーがそのデータ ソース コンピューターへのアクセス許可を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="0dbe5-p101">Make sure the directories accessed by IIS have proper permissions. RDS can communicate with an IIS Web server running in any one of the three Password Authentication modes: Anonymous, Basic, or NT Challenge/Response (called Integrated Windows authentication in Windows 2000). Also, the Web server must have permissions to the data source computer if it is a Windows NT/Windows 2000 computer.</span></span>

