---
title: クエリ メソッド (RDS - Access デスクトップ データベースリファレンス)
TOCTitle: Query method (RDS)
ms:assetid: c88d82bd-2139-7f1e-4e5e-9030f3795816
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249975(v=office.15)
ms:contentKeyID: 48547658
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 965dbe7736483c6e2cc926ec4f9fc037e503089b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562427"
---
# <a name="query-method-rds"></a>クエリ メソッド (RDS)

**適用先:** Access 2013、Office 2013

有効な SQL クエリ文字列を使用して [Recordset](recordset-object-ado.md) を返します。

## <a name="syntax"></a>構文

Set *Recordset*  =  *DataFactory*.Query(*Connection*, *Query*)

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Recordset* |**Recordset** オブジェクトを表すオブジェクト変数を指定します。|
|*DataFactory* |[RDSServer.DataFactory](datafactory-object-rdsserver.md) オブジェクトを表すオブジェクト変数。|
|*Connection* |サーバー接続情報を含む文字列型 ( **String** ) の値を指定します。このパラメーターは [Connect](connect-property-rds.md) プロパティに似ています。|
|*Query* |SQL クエリを含む文字列型 ( **String** ) の値を指定します。|

## <a name="remarks"></a>注釈

クエリでは、データベース サーバーの SQL 文法を使用する必要があります。実行したクエリにエラーがある場合は、結果のステータスが返されます。**Query** メソッドでは、**Query** 文字列の構文チェックは行われません。

