---
title: Query メソッド (RDS のデスクトップのデータベース参照のアクセス)
TOCTitle: Query method (RDS)
ms:assetid: c88d82bd-2139-7f1e-4e5e-9030f3795816
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249975(v=office.15)
ms:contentKeyID: 48547658
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1e7f9dfc3ce5cb0d757951f13c1078ab44d04760
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949426"
---
# <a name="query-method-rds"></a>Query メソッド (RDS)

**適用されます**Access 2013、Office 2013。

有効な SQL クエリ文字列を使用して [Recordset](recordset-object-ado.md) を返します。

## <a name="syntax"></a>構文

*レコード セット*を設定する = *DataFactory*。クエリ (*接続*、*クエリ*)

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Recordset* |**Recordset** オブジェクトを表すオブジェクト変数を指定します。|
|*DataFactory* |[RDSServer.DataFactory](datafactory-object-rdsserver.md) オブジェクトを表すオブジェクト変数を指定します。|
|*Connection* |サーバー接続情報を含む文字列型 ( **String** ) の値を指定します。このパラメーターは [Connect](connect-property-rds.md) プロパティに似ています。|
|*Query* |SQL クエリを含む文字列型 ( **String** ) の値を指定します。|

## <a name="remarks"></a>解説

クエリでは、データベース サーバーの SQL 文法を使用する必要があります。実行したクエリにエラーがある場合は、結果のステータスが返されます。 **Query** メソッドでは、 **Query** 文字列の構文チェックは行われません。

