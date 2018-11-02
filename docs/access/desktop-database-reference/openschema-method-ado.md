---
title: OpenSchema メソッド (ADO)
TOCTitle: OpenSchema method (ADO)
ms:assetid: 57771163-a14e-207a-2942-849acb79a9a1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249294(v=office.15)
ms:contentKeyID: 48544970
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 846d1c0f73ba4a17f166fffc7c1bb4682ad31d49
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921167"
---
# <a name="openschema-method-ado"></a>OpenSchema メソッド (ADO)


**適用されます**Access 2013、Office 2013。


プロバイダーからデータベースのスキーマ情報を取得します。

## <a name="syntax"></a>構文

**設定。 レコード セット* = *接続*します。OpenSchema (* QueryType *、*条件*、 *SchemaID*)

## <a name="return-values"></a>戻り値

スキーマ情報を含む [Recordset](recordset-object-ado.md) オブジェクトを返します。 **Recordset** は読み取り専用の静的カーソルとして開かれます。 *QueryType*は、**レコード セット**に表示する列を決定します。

## <a name="parameters"></a>パラメーター

  - *QueryType*

  - 実行するスキーマ クエリの種類を表す [SchemaEnum](schemaenum.md) 値を指定します。

  - *Criteria*

  - 省略可能です。 **SchemaEnum**に記載されている各*QueryType*オプション、クエリの制約の配列。

  - *SchemaID*

  - OLE DB 仕様で定義されていないプロバイダー スキーマ クエリの GUID です。 *QueryType*が**adSchemaProviderSpecific**; に設定されている場合、このパラメーターが必要ですそれ以外の場合は使用されません。

## <a name="remarks"></a>解説

**OpenSchema** メソッドは、データ ソースに含まれるテーブル、テーブルに含まれる列、サポートされているデータ型などのデータ ソースに関する情報を返します。

*QueryType*引数は、列 (スキーマ) が返されるかを示す GUID です。 OLE DB の仕様には、すべてのスキーマの一覧があります。

引数*Criteria*は、スキーマ クエリの結果を制限します。 *条件*では、列、*制約の列*、結果の**レコード セット**内の対応するサブセットで行う必要のある値の配列を指定します。

プロバイダーが上記以外の独自の非標準スキーマ クエリを定義する場合は、 *QueryType*引数の定数**adSchemaProviderSpecific**が使用されます。 この定数を使用する場合に実行するスキーマ クエリの GUID を渡す、 *SchemaID*引数が必要です。 *QueryType*が**adSchemaProviderSpecific**に設定されて場合は、 *SchemaID*が指定されていないエラーが発生します。

プロバイダーは、すべての OLE DB 標準スキーマ クエリをサポートする必要はありません。 OLE DB の仕様では、 **adSchemaTables** 、 **adSchemaColumns** 、および **adSchemaProviderTypes** のみが必要とされます。 ただし、プロバイダーは*Criteria*の制約上これらのスキーマ クエリをサポートする必要はありません。

**リモート データ サービスの使用法****OpenSchema**メソッドがクライアント側の[Connection](connection-object-ado.md)オブジェクトで使用可能ではありません。


> [!NOTE]
> <P>Visual Basic では、 <STRONG>Connection</STRONG>オブジェクトの<STRONG>OpenSchema</STRONG>メソッドから返される<STRONG>レコード セット</STRONG>では 4 バイトの符号なし整数 (DBTYPE UI4) が設定されている列は他の変数を比較できません。 OLE DB データ型の詳細については、第 13 章と付録 A の<EM>Microsoft OLE DB プログラマ リファレンス</EM>を参照してください。</P>


