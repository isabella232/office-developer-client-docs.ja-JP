---
title: Open メソッド (ADO Connection)
TOCTitle: Open method (ADO Connection)
ms:assetid: 1adaa17d-dfe1-22e0-3415-720516d138f8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248951(v=office.15)
ms:contentKeyID: 48543525
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b3b83eb87b181320c86e1aea91ede70cd173a5ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288428"
---
# <a name="open-method-ado-connection"></a>Open メソッド (ADO Connection)

**適用先:** Access 2013、Office 2013
 
データ ソースへの接続を開きます。

## <a name="syntax"></a>構文

*接続*。開いている*ConnectionString*、*ユーザー id*、*パスワード*、*オプション*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*ConnectionString* |省略可能です。接続情報を含む文字列型 ( **String** ) の値です。有効な設定値の詳細については、 [ConnectionString](connectionstring-property-ado.md) プロパティを参照してください。|
|*UserID* |省略可能です。接続を確立するときに使用するユーザー名を含む、文字列型 ( **String** ) の値です。|
|*Password* |省略可能です。接続を確立するときに使用するパスワードを含む、文字列型 ( **String** ) の値です。|
|*Options* |省略可能です。接続が確立された後 (同期) または接続が確立される前 (非同期) のどちらでこのメソッドが返るかを指定する [ConnectOptionEnum](connectoptionenum.md) 値です。|

## <a name="remarks"></a>注釈

[Connection](connection-object-ado.md) オブジェクトで **Open** メソッドを使用すると、データ ソースへの物理的な接続が確立されます。このメソッドが正常に終了すると、接続が有効になり、接続に対してコマンドを発行して、その結果を処理することができます。

省略可能な*ConnectionString*引数を使用して、セミコロンで区切られた一連の*引数* *= value*ステートメントを含む接続文字列を指定するか、または URL で識別されるファイルまたはディレクトリリソースを指定します。 **connectionstring**プロパティは、 *connectionstring*引数に使用された値を自動的に継承します。 そのため、 **connection**オブジェクトを開く前に、 **connectionstring**プロパティを設定するか、または*connectionstring*引数を使用して、 **Open**メソッドの呼び出し中に現在の接続パラメーターを設定または上書きすることができます。.

ユーザーとパスワードの情報を、*ConnectionString* 引数と、省略可能な *UserID* 引数および *Password* 引数の両方で渡すと、*UserID* 引数と *Password* 引数の方が、*ConnectionString* で指定した値より優先されます。

開いている **Connection** オブジェクトに対する操作が完了したら、[Close](close-method-ado.md) メソッドを使用して関連するすべてのシステム リソースを解放します。オブジェクトを閉じても、オブジェクトはメモリから削除されません。オブジェクトのプロパティ設定を変更し、**Open** メソッドを使用して、後で再度開くことができます。オブジェクトをメモリから完全に削除するには、オブジェクト変数に *Nothing* を設定します。

**リモートデータサービスの使用状況**クライアント側の**connection**オブジェクトで使用する場合、 **connection**オブジェクトで[Recordset](recordset-object-ado.md)が開かれるまで、 **Open**メソッドは実際にはサーバーへの接続を確立しません。

> [!NOTE]
> [!メモ] http スキームを使用している URL は、[Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) を自動的に呼び出します。 詳細については、「[絶対 url と相対 url](absolute-and-relative-urls.md)」を参照してください。


