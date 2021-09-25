---
title: 'インターネット サーバー エラー: アクセスが拒否されました'
TOCTitle: 'Internet Server Error: Access Denied'
ms:assetid: 65f4608b-afec-2867-dae3-e29bae03a6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249395(v=office.15)
ms:contentKeyID: 48545334
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c0b10a07370d2c963328114543b598aa9af9ac26
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594070"
---
# <a name="internet-server-error-access-denied"></a>インターネット サーバー エラー: アクセスが拒否されました


**適用先**: Access 2013、Office 2013

このエラーが発生した場合は、通常、Microsoft インターネット インフォメーション サービス (IIS) が次の状態を返したことを意味します。

HTTP \_ 状態 \_ が拒否されました 401

IIS がアクセスしているディレクトリが適切なアクセス許可を持っているかどうかを確認してください。 RDS は、匿名、基本、または NT チャレンジ/応答 (Windows 2000 の統合 Windows 認証と呼ばれる) のいずれかの 3 つのパスワード認証モードで実行されている IIS Web サーバーと通信できます。 また、Web サーバーが 2000 台のコンピューターの場合は、データ ソース コンピューター Windows NT/Windows必要があります。

