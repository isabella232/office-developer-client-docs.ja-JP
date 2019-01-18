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
# <a name="internet-server-error-access-denied"></a>インターネット サーバー エラー: アクセスが拒否されました


**適用されます**Access 2013、Office 2013。

このエラーが発生した場合は、通常、Microsoft インターネット インフォメーション サービス (IIS) が次の状態を返したことを意味します。

HTTP\_ステータス\_401 は拒否されました

IIS がアクセスしているディレクトリが適切なアクセス許可を持っているかどうかを確認してください。 RDS は、次の 3 つのパスワード認証モードのいずれかで実行されている IIS web サーバーと通信できます。 匿名、基本、または NT チャレンジ/レスポンス (Windows 2000 では統合 Windows 認証と呼ばれます)。 Web サーバーは、Windows NT または Windows 2000 コンピューターである場合、データの送信元のコンピューターへのアクセス許可が必要です。

