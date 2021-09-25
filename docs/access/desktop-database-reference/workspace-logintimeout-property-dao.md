---
title: Workspace.LoginTimeout プロパティ (DAO)
TOCTitle: LoginTimeout Property
ms:assetid: 5f03b166-abbc-20de-1a01-3869a9f2907d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194743(v=office.15)
ms:contentKeyID: 48545151
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 841346da6d78389f52bc4c7882e5cfc8a0b0f945
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552375"
---
# <a name="workspacelogintimeout-property-dao"></a>Workspace.LoginTimeout プロパティ (DAO)


**適用先:** Access 2013、Office 2013

ODBC データベースへのログオン試行でエラーが発生するまでの秒数を設定または取得します。

## <a name="syntax"></a>構文

*式* .LoginTimeout

*expression*: **Workspace** オブジェクトを表す変数。

## <a name="remarks"></a>注釈

**LoginTimeout** プロパティの既定の設定値は 20 秒です。 **LoginTimeout** プロパティを 0 に設定すると、タイムアウトは発生しません。

Microsoft SQL Server などの ODBC データベースにログオンしようとすると、ネットワーク エラーが発生するか、サーバーが動作していないために、接続が失敗する可能性があります。既定の 20 秒間待機してから接続するのではなく、待機する時間を指定し、それを超えたらエラーとすることができます。サーバーへのログオンは、外部サーバー データベースでのクエリの実行など、多数の異なるイベントの一環として暗黙に実行されます。

