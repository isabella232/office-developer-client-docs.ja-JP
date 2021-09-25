---
title: Open メソッド (ADO Connection)
TOCTitle: Open method (ADO Connection)
ms:assetid: 1adaa17d-dfe1-22e0-3415-720516d138f8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248951(v=office.15)
ms:contentKeyID: 48543525
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 45d41395759039fa664caeb5950931e8e39e3cc4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558185"
---
# <a name="open-method-ado-connection"></a>Open メソッド (ADO Connection)

**適用先:** Access 2013、Office 2013
 
データ ソースへの接続を開きます。

## <a name="syntax"></a>構文

*接続*.Open *ConnectionString*, *UserID*, *Password*, *Options*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*ConnectionString* |省略可能です。接続情報を含む文字列型 ( **String** ) の値です。有効な設定値の詳細については、 [ConnectionString](connectionstring-property-ado.md) プロパティを参照してください。|
|*UserID* |省略可能です。接続を確立するときに使用するユーザー名を含む、文字列型 ( **String** ) の値です。|
|*Password* |省略可能です。接続を確立するときに使用するパスワードを含む、文字列型 ( **String** ) の値です。|
|*Options* |省略可能です。接続が確立された後 (同期) または接続が確立される前 (非同期) のどちらでこのメソッドが返るかを指定する [ConnectOptionEnum](connectoptionenum.md) 値です。|

## <a name="remarks"></a>注釈

[Connection](connection-object-ado.md) オブジェクトで **Open** メソッドを使用すると、データ ソースへの物理的な接続が確立されます。このメソッドが正常に終了すると、接続が有効になり、接続に対してコマンドを発行して、その結果を処理することができます。

オプションの *ConnectionString* 引数を使用して、セミコロンで区切られた一連の引数 *= value* ステートメントを含む接続文字列、または URL で識別されるファイルまたはディレクトリ リソースを指定します。 **ConnectionString プロパティは、ConnectionString** 引数に使用される値 *を自動的に継承* します。 そのため **、Connection** オブジェクトを開く前に Connection オブジェクトの **ConnectionString** プロパティを設定するか、*引数 ConnectionString* を使用して **、Open** メソッドの呼び出し中に現在の接続パラメーターを設定または上書きできます。

ユーザーとパスワードの情報を、*ConnectionString* 引数と、省略可能な *UserID* 引数および *Password* 引数の両方で渡すと、*UserID* 引数と *Password* 引数の方が、*ConnectionString* で指定した値より優先されます。

開いている **Connection** オブジェクトに対する操作が完了したら、[Close](close-method-ado.md) メソッドを使用して関連するすべてのシステム リソースを解放します。オブジェクトを閉じても、オブジェクトはメモリから削除されません。オブジェクトのプロパティ設定を変更し、**Open** メソッドを使用して、後で再度開くことができます。オブジェクトをメモリから完全に削除するには、オブジェクト変数に *Nothing* を設定します。

**リモート データ サービスの使用状況** クライアント側の **Connection** オブジェクトで使用する場合 **、Open** メソッドは [、Connection](recordset-object-ado.md) オブジェクトで Recordset を開くまで、実際にはサーバーへの接続を **確立** しません。

> [!NOTE]
> [!メモ] http スキームを使用している URL は、[Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) を自動的に呼び出します。 詳細については、「絶対 URL と [相対 URL」を参照してください](absolute-and-relative-urls.md)。


