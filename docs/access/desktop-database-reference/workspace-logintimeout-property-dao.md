---
title: Workspace.LoginTimeout プロパティ (DAO)
TOCTitle: LoginTimeout Property
ms:assetid: 5f03b166-abbc-20de-1a01-3869a9f2907d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194743(v=office.15)
ms:contentKeyID: 48545151
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6427b99fd212fa358b70fb20a5ecf0c9180209fb
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476255"
---
# <a name="workspacelogintimeout-property-dao"></a>Workspace.LoginTimeout プロパティ (DAO)


**適用されます**Access 2013 |。Office 2013

ODBC データベースへのログオンを試みてからエラーが発生するまでの秒数を設定または取得します。

## <a name="syntax"></a>構文

*式*です。LoginTimeout

*式***ワークスペース**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

**LoginTimeout** プロパティの既定の設定は 20 秒です。 **LoginTimeout** プロパティを 0 に設定すると、タイムアウトは発生しません。

Microsoft SQL Server などの ODBC データベースへのログオンを試みたときに、ネットワーク エラーが発生したりサーバーが実行中でないことが原因で、接続に失敗したりする場合があります。接続時に既定の 20 秒間待機する代わりに、エラーが発生するまでの時間を指定できます。外部のサーバー データベースに対するクエリの実行など、多くのさまざまなイベントの一部として、サーバーへの暗黙的なログオンが発生します。

