---
title: 'インターネット サーバー エラー: アクセスは拒否されました'
TOCTitle: 'Internet Server Error: Access Denied'
ms:assetid: 65f4608b-afec-2867-dae3-e29bae03a6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249395(v=office.15)
ms:contentKeyID: 48545334
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c874b7a2c4facb9f5969bf9a2150c86773a2687a
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603344"
---
# <a name="internet-server-error-access-denied"></a>インターネット サーバー エラー: アクセスは拒否されました


**適用されます**Access 2013 |。Office 2013

このエラーが発生した場合は、通常、Microsoft インターネット インフォメーション サービス (IIS) が次の状態を返したことを意味します。

HTTP\_ステータス\_401 は拒否されました

<<<<<<< ヘッドは、IIS がアクセスしているディレクトリは、適切なアクセス許可を持っていることを確認します。 RDS は、匿名、基本、または NT チャレンジ/レスポンス (Windows 2000 では統合 Windows 認証) の 3 種類のパスワード認証モードで実行している IIS Web サーバーと通信できます。 また、データ ソース コンピューターが Windows NT/Windows 2000 コンピューターの場合、Web サーバーがそのデータ ソース コンピューターへのアクセス許可を持っている必要があります。
===、適切なアクセス許可を IIS がアクセスしているディレクトリがあることを確認します。 RDS は、次の 3 つのパスワード認証モードのいずれかで実行されている IIS web サーバーと通信できます。 匿名、基本、または NT チャレンジ/レスポンス (Windows 2000 では統合 Windows 認証と呼ばれます)。 Web サーバーは、Windows NT または Windows 2000 コンピューターである場合、データの送信元のコンピューターへのアクセス許可が必要です。
>>>>>>> master

