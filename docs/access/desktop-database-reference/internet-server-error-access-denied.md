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
# <a name="internet-server-error-access-denied"></a>インターネット サーバー エラー: アクセスが拒否されました


**適用されます**Access 2013、Office 2013。

このエラーが発生した場合は、通常、Microsoft インターネット インフォメーション サービス (IIS) が次の状態を返したことを意味します。

HTTP\_ステータス\_401 は拒否されました

IIS がアクセスしているディレクトリが適切なアクセス許可を持っているかどうかを確認してください。 RDS は、次の 3 つのパスワード認証モードのいずれかで実行されている IIS web サーバーと通信できます。 匿名、基本、または NT チャレンジ/レスポンス (Windows 2000 では統合 Windows 認証と呼ばれます)。 Web サーバーは、Windows NT または Windows 2000 コンピューターである場合、データの送信元のコンピューターへのアクセス許可が必要です。

