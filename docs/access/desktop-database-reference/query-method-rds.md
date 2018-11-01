---
title: Query メソッド (RDS のデスクトップのデータベース参照のアクセス)
TOCTitle: Query Method (RDS)
ms:assetid: c88d82bd-2139-7f1e-4e5e-9030f3795816
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249975(v=office.15)
ms:contentKeyID: 48547658
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 70f4a1c7a16a97710ef2b0c04bbc0a3924864231
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876030"
---
# <a name="query-method-rds"></a>Query メソッド (RDS)


**適用されます**Access 2013、Office 2013。


有効な SQL クエリ文字列を使用して [Recordset](recordset-object-ado.md) を返します。

## <a name="syntax"></a>構文

*レコード セット*を設定する = *DataFactory*。クエリ (*接続*、*クエリ*)

## <a name="parameters"></a>パラメーター

  - *Recordset*

  - **Recordset** オブジェクトを表すオブジェクト変数を指定します。

  - *DataFactory*

  - [RDSServer.DataFactory](datafactory-object-rdsserver.md) オブジェクトを表すオブジェクト変数を指定します。

  - *Connection*

  - サーバー接続情報を含む文字列型 ( **String** ) の値を指定します。このパラメーターは [Connect](connect-property-rds.md) プロパティに似ています。

  - *Query*

  - SQL クエリを含む文字列型 ( **String** ) の値を指定します。

## <a name="remarks"></a>解説

クエリでは、データベース サーバーの SQL 文法を使用する必要があります。実行したクエリにエラーがある場合は、結果のステータスが返されます。 **Query** メソッドでは、 **Query** 文字列の構文チェックは行われません。

