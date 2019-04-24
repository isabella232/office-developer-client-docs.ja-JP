---
title: Workspace タイムアウトプロパティ (DAO)
TOCTitle: LoginTimeout Property
ms:assetid: 5f03b166-abbc-20de-1a01-3869a9f2907d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194743(v=office.15)
ms:contentKeyID: 48545151
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: dbc0ed4849e8c22bc7023bd4254fdee74a5d016c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306910"
---
# <a name="workspacelogintimeout-property-dao"></a>Workspace タイムアウトプロパティ (DAO)


**適用先:** Access 2013、Office 2013

ODBC データベースへのログオン試行でエラーが発生するまでの秒数を設定または取得します。

## <a name="syntax"></a>構文

*式*。LoginTimeout

*式***Workspace**オブジェクトを表す変数を取得します。

## <a name="remarks"></a>注釈

**LoginTimeout** プロパティの既定の設定値は 20 秒です。 **LoginTimeout** プロパティを 0 に設定すると、タイムアウトは発生しません。

Microsoft SQL Server などの ODBC データベースにログオンしようとすると、ネットワーク エラーが発生するか、サーバーが動作していないために、接続が失敗する可能性があります。既定の 20 秒間待機してから接続するのではなく、待機する時間を指定し、それを超えたらエラーとすることができます。サーバーへのログオンは、外部サーバー データベースでのクエリの実行など、多数の異なるイベントの一環として暗黙に実行されます。

