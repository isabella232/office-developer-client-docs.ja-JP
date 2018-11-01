---
title: Connection.QueryTimeout プロパティ (DAO)
TOCTitle: QueryTimeout Property
ms:assetid: 97853412-d5ae-7a71-ccaa-595c68919654
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197804(v=office.15)
ms:contentKeyID: 48546471
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052905
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 8f5ce9faa1ebd56bdc8e4de5aeea417835c950b7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878809"
---
# <a name="connectionquerytimeout-property-dao"></a>Connection.QueryTimeout プロパティ (DAO)


**適用されます**Access 2013、Office 2013。

ODBC データ ソースでクエリが実行される場合の、タイムアウト エラーが発生するまでに待機する秒数を指定する値を設定または取得します。

## <a name="syntax"></a>構文

*式*です。QueryTimeout

*式***接続**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

既定値は 60 です。

Microsoft SQL Server などの ODBC データベースを使用している場合、ネットワーク トラフィックや ODBC サーバーに対する負荷の増大のために、応答が遅れることがあります。無限に待機せずに、待機する時間を指定できます。

[**Connection**](connection-object-dao.md) オブジェクトまたは [**Database**](database-object-dao.md) オブジェクトで **QueryTimeout** プロパティを使用する場合、データベースに関連付けられているすべてのクエリに対してグローバル値を指定します。特定の [**QueryDef**](querydef-object-dao.md) オブジェクトの **ODBCTimeout** プロパティを設定すると、特定のクエリに対してこのグローバル値より優先させることができます。

