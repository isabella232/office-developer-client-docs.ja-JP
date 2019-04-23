---
title: OpenSchema メソッド (ADO)
TOCTitle: OpenSchema method (ADO)
ms:assetid: 57771163-a14e-207a-2942-849acb79a9a1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249294(v=office.15)
ms:contentKeyID: 48544970
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 43ca69b9d761629d42138780517f8de806ed7e8c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288337"
---
# <a name="openschema-method-ado"></a>OpenSchema メソッド (ADO)

**適用先:** Access 2013、Office 2013

プロバイダーからデータベースのスキーマ情報を取得します。

## <a name="syntax"></a>構文

**Set * * * recordset* = *接続*。OpenSchema (* QueryType *、 *Criteria*、 *schemaid*)

## <a name="return-values"></a>戻り値

スキーマ情報を含む [Recordset](recordset-object-ado.md) オブジェクトを返します。 **Recordset** は読み取り専用の静的カーソルとして開かれます。 *QueryType* により、**Recordset** に表示される列が決まります。

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*QueryType* |実行するスキーマ クエリの種類を表す [SchemaEnum](schemaenum.md) 値を指定します。|
|*Criteria* |省略可能です。 **SchemaEnum** の指定に従って、各 *QueryType* オプションのクエリ制約の配列を指定します。|
|*SchemaID* |OLE DB の仕様で定義されていない、プロバイダー スキーマのクエリの GUID (グローバル一意識別子) を指定します。このパラメーターは、*QueryType* が **adSchemaProviderSpecific** に設定されている場合は必須です。それ以外の場合、このパラメーターは使用しません。|

## <a name="remarks"></a>注釈

**OpenSchema** メソッドは、データ ソースに含まれるテーブル、テーブルに含まれる列、サポートされているデータ型などのデータ ソースに関する情報を返します。

*QueryType* 引数は、返される列 (スキーマ) を示す GUID です。OLE DB の仕様には、すべてのスキーマの一覧があります。

引数*Criteria*は、スキーマクエリの結果を制限します。 *Criteria*には、結果の**Recordset**で、対応する列の列のサブセット (*制約列*) に必要な値の配列を指定します。

OLE DB 仕様以外の非標準スキーマ クエリをプロバイダーが独自に定義している場合は、*QueryType* 引数に **adSchemaProviderSpecific** を使用します。この定数を使用する場合は、*SchemaID* 引数に、実行するスキーマ クエリの GUID を指定する必要があります。*QueryType* が **adSchemaProviderSpecific** に設定され、*SchemaID* が指定されていない場合、エラーが発生します。

プロバイダーは、すべての OLE DB 標準スキーマ クエリをサポートする必要はありません。OLE DB の仕様では、**adSchemaTables**、**adSchemaColumns**、および **adSchemaProviderTypes** のみが必要とされます。ただし、これらのスキーマ クエリでは、プロバイダーは *Criteria* の制約をサポートする必要はありません。

**リモートデータサービスの使用状況****OpenSchema**メソッドは、クライアント側の[Connection](connection-object-ado.md)オブジェクトでは使用できません。

> [!NOTE]
> In Visual Basic, columns that have a four-byte unsigned integer (DBTYPE UI4) in the **Recordset** returned from the **OpenSchema** method on the **Connection** object cannot be compared to other variables. ole db データ型の詳細については、「 *Microsoft ole db プログラマリファレンス*」の「第13章」および「付録 a」を参照してください。


