---
title: Open メソッド (ADO Record)
TOCTitle: Open method (ADO Record)
ms:assetid: ba71c5c7-326e-d3b6-0e74-e8343ee6896f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249896(v=office.15)
ms:contentKeyID: 48547371
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 87fe3e50c6abc0d78f1bf506c02bc63829fec882
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602116"
---
# <a name="open-method-ado-record"></a>Open メソッド (ADO Record)

**適用先**: Access 2013、Office 2013

既存の [Record](record-object-ado.md) オブジェクトを開くか、または **Record** で表される新しいアイテム (ファイル、ディレクトリなど) を作成します。

## <a name="syntax"></a>構文

オープン *ソース*、 *ActiveConnection*、 *Mode*、 *CreateOptions*、 *Options*、 *UserName*、 *Password*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Source* |省略可能です。 **Record** オブジェクトで表されるエンティティの URL、 **Command** 、開かれた **Recordset** または別の [Record](recordset-object-ado.md) オブジェクト、SQL SELECT ステートメントを含む文字列、またはテーブル名を表すバリアント型 ( **Variant** ) の値を指定します。|
|*ActiveConnection* | 省略可能です。接続文字列または開かれた **Connection** オブジェクトを表すバリアント型 ( [Variant](connection-object-ado.md) ) の値を指定します。|
|*Mode* |省略可能です。結果の [Record](connectmodeenum.md) オブジェクトのアクセス モードを **ConnectModeEnum** 値で指定します。既定値は **adModeUnknown** です。|
|*CreateOptions* |省略可能です。既存のファイルまたはディレクトリを開くか、新しいファイルまたはディレクトリを作成するかを、[RecordCreateOptionsEnum](recordcreateoptionsenum.md) 値で指定します。既定値は **adFailIfNotExists** です。既定値の場合、アクセス モードは [Mode](mode-property-ado.md) プロパティから取得されます。このパラメーターは、*Source* パラメーターに URL が含まれていないと無視されます。|
|*Options* |省略可能です。 [Record](recordopenoptionsenum.md) を開くときのオプションを **RecordOpenOptionsEnum** 値で指定します。既定値は **adOpenRecordUnspecified** です。これらの値は組み合わせることもできます。|
|*UserName* |省略可能です。*Source* へのアクセス権が設定されている場合、アクセス権を持つユーザー ID を含む、文字列型 (**String**) の値を指定します。|
|*Password* |省略可能です。*UserName* を確認するためのパスワードを含む、文字列型 (**String**) の値を指定します。|

## <a name="remarks"></a>注釈

*Source* には、次の値を指定できます。

- URL。URL のプロトコルが http の場合、既定ではインターネット プロバイダーが呼び出されます。URL が実行可能スクリプト (拡張子が .ASP のページなど) を含むノードを指している場合、既定では実行されたコンテンツではなく、そのソースを含む **Record** が開かれます。この動作は *Options* 引数を使用して修正します。

- **Record** オブジェクト。別の **Record** から開かれた **Record** オブジェクトは、元の **Record** オブジェクトを複製します。

- **Command** オブジェクト。開かれた **Record** オブジェクトは、 **Command** を実行することによって返された単一の行を表します。結果に複数の行が含まれる場合、レコードには最初の行の内容が入り、 **Errors** コレクションにエラーが追加されることがあります。

- SQL SELECT ステートメント。開かれた **Record** オブジェクトは、文字列の内容を実行することによって返された単一の行を表します。結果に複数の行が含まれる場合、レコードには最初の行の内容が入り、 **Errors** コレクションにエラーが追加されることがあります。

- テーブル名。

**Record** オブジェクトが、URL でアクセスできないエンティティ (データベースから派生した **Recordset** の行など) を表す場合、 [ParentURL](parenturl-property-ado.md) プロパティの値、および **adRecordURL** 定数でアクセスするフィールドの値はいずれも Null になります。

> [!NOTE]
> [!メモ] http 体系を使用している URL は、[Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) を自動的に呼び出します。 詳細については、「絶対 URL と [相対 URL」を参照してください](absolute-and-relative-urls.md)。


