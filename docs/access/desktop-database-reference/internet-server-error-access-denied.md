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
# <a name="internet-server-error-access-denied"></a>インターネット サーバー エラー: アクセスが拒否されました


**適用先:** Access 2013、Office 2013

このエラーが発生した場合は、通常、Microsoft インターネット インフォメーション サービス (IIS) が次の状態を返したことを意味します。

HTTP\_状態\_の拒否401

IIS がアクセスしているディレクトリが適切なアクセス許可を持っているかどうかを確認してください。 RDS は、匿名、基本、または NT チャレンジ/レスポンス (windows 2000 では統合 Windows 認証と呼ばれます) の3つのパスワード認証モードのいずれかで実行されている IIS web サーバーと通信できます。 また、web サーバーが windows NT/windows 2000 コンピューターの場合は、データソースコンピューターへのアクセス許可が必要です。

