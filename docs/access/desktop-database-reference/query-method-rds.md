---
title: Query メソッド (RDS-Access デスクトップデータベースリファレンス)
TOCTitle: Query method (RDS)
ms:assetid: c88d82bd-2139-7f1e-4e5e-9030f3795816
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249975(v=office.15)
ms:contentKeyID: 48547658
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 92c72bf78f8f01a675038f63b065aceb6869fcd0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301114"
---
# <a name="query-method-rds"></a>Query メソッド (RDS)

**適用先:** Access 2013、Office 2013

有効な SQL クエリ文字列を使用して [Recordset](recordset-object-ado.md) を返します。

## <a name="syntax"></a>構文

*Recordset* = *DataFactory*を設定します。クエリ (*接続*、*クエリ*)

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Recordset* |**Recordset** オブジェクトを表すオブジェクト変数を指定します。|
|*DataFactory* |[RDSServer.DataFactory](datafactory-object-rdsserver.md) オブジェクトを表すオブジェクト変数。|
|*Connection* |サーバー接続情報を含む文字列型 ( **String** ) の値を指定します。このパラメーターは [Connect](connect-property-rds.md) プロパティに似ています。|
|*Query* |SQL クエリを含む文字列型 ( **String** ) の値を指定します。|

## <a name="remarks"></a>注釈

クエリでは、データベース サーバーの SQL 文法を使用する必要があります。実行したクエリにエラーがある場合は、結果のステータスが返されます。**Query** メソッドでは、**Query** 文字列の構文チェックは行われません。

