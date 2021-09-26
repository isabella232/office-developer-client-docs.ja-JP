---
title: DBEngine.LoginTimeout プロパティ (DAO)
TOCTitle: LoginTimeout Property
ms:assetid: 81d14153-79c5-7860-b6a8-4079d2d7acf7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196648(v=office.15)
ms:contentKeyID: 48545964
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052923
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 631459d65e9064f68b5d5e445db148748411136f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589695"
---
# <a name="dbenginelogintimeout-property-dao"></a>DBEngine.LoginTimeout プロパティ (DAO)


**適用先**: Access 2013、Office 2013

ODBC データベースへのログオン試行でエラーが発生するまでの秒数を設定または取得します。

## <a name="syntax"></a>構文

*式* .LoginTimeout

*式* **DBEngine** オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

**LoginTimeout** プロパティの既定の設定値は 20 秒です。 **LoginTimeout** プロパティを 0 に設定すると、タイムアウトは発生しません。

Microsoft SQL Server などの ODBC データベースにログオンしようとすると、ネットワーク エラーが発生するか、サーバーが動作していないために、接続が失敗する可能性があります。既定の 20 秒間待機してから接続するのではなく、待機する時間を指定し、それを超えたらエラーとすることができます。サーバーへのログオンは、外部サーバー データベースでのクエリの実行など、多数の異なるイベントの一環として暗黙に実行されます。

