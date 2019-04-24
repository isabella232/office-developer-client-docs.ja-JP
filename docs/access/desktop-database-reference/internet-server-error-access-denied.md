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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291256"
---
# <a name="internet-server-error-access-denied"></a><span data-ttu-id="4ae48-102">インターネット サーバー エラー: アクセスが拒否されました</span><span class="sxs-lookup"><span data-stu-id="4ae48-102">Internet Server error: Access Denied</span></span>


<span data-ttu-id="4ae48-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="4ae48-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4ae48-104">このエラーが発生した場合は、通常、Microsoft インターネット インフォメーション サービス (IIS) が次の状態を返したことを意味します。</span><span class="sxs-lookup"><span data-stu-id="4ae48-104">If you get this error, it usually means that Microsoft Internet Information Services (IIS) returned the following status:</span></span>

<span data-ttu-id="4ae48-105">HTTP\_状態\_の拒否401</span><span class="sxs-lookup"><span data-stu-id="4ae48-105">HTTP\_STATUS\_DENIED 401</span></span>

<span data-ttu-id="4ae48-106">IIS がアクセスしているディレクトリが適切なアクセス許可を持っているかどうかを確認してください。</span><span class="sxs-lookup"><span data-stu-id="4ae48-106">Make sure the directories accessed by IIS have proper permissions.</span></span> <span data-ttu-id="4ae48-107">RDS は、匿名、基本、または NT チャレンジ/レスポンス (windows 2000 では統合 Windows 認証と呼ばれます) の3つのパスワード認証モードのいずれかで実行されている IIS web サーバーと通信できます。</span><span class="sxs-lookup"><span data-stu-id="4ae48-107">RDS can communicate with an IIS web server running in any one of the three Password Authentication modes: Anonymous, Basic, or NT Challenge/Response (called Integrated Windows authentication in Windows 2000).</span></span> <span data-ttu-id="4ae48-108">また、web サーバーが windows NT/windows 2000 コンピューターの場合は、データソースコンピューターへのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="4ae48-108">Also, the web server must have permissions to the data source computer if it is a Windows NT/Windows 2000 computer.</span></span>

