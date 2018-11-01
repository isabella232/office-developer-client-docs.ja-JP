---
title: Open メソッド (ADO Connection)
TOCTitle: Open Method (ADO Connection)
ms:assetid: 1adaa17d-dfe1-22e0-3415-720516d138f8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248951(v=office.15)
ms:contentKeyID: 48543525
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3bd698f7ea6c05d81e07969ae8031049804b7706
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889470"
---
# <a name="open-method-ado-connection"></a>Open メソッド (ADO Connection)


**適用されます**Access 2013、Office 2013。
 

データ ソースへの接続を開きます。

## <a name="syntax"></a>構文

*接続*します。*接続文字列*、*ユーザー Id*、*パスワード**のオプション*を開く

## <a name="parameters"></a>パラメーター

  - *ConnectionString*

  - 省略可能です。接続情報を含む文字列型 ( **String** ) の値です。有効な設定値の詳細については、 [ConnectionString](connectionstring-property-ado.md) プロパティを参照してください。

  - *ユーザー Id*

  - 省略可能です。接続を確立するときに使用するユーザー名を含む、文字列型 ( **String** ) の値です。

  - *Password*

  - 省略可能です。接続を確立するときに使用するパスワードを含む、文字列型 ( **String** ) の値です。

  - *Options*

  - 省略可能です。接続が確立された後 (同期) または接続が確立される前 (非同期) のどちらでこのメソッドが返るかを指定する [ConnectOptionEnum](connectoptionenum.md) 値です。

## <a name="remarks"></a>解説

**Connection** オブジェクトで [Open](connection-object-ado.md) メソッドを使用すると、データ ソースへの物理的な接続が確立されます。このメソッドが正常に終了すると、接続が有効になり、接続に対してコマンドを発行して、その結果を処理することができます。

一連の*引数* *= 値*ステートメントを指定するセミコロン、またはファイルまたは URL で識別されるリソースはディレクトリを含む接続文字列を指定するのに省略可能な*ConnectionString*引数を使用します。 **ConnectionString**プロパティは、 *ConnectionString*引数に対して使用する値を自動的に継承します。 したがって、開く前に**Connection**オブジェクトの**ConnectionString**プロパティを設定するか、 **Open**メソッドの呼び出し時に現在の接続パラメーターのオーバーライドを設定または*接続文字列*の引数を使用して.

ユーザーとパスワードの情報を、*ConnectionString* 引数と、省略可能な *UserID* 引数および *Password* 引数の両方で渡すと、*UserID* 引数と *Password* 引数の方が、*ConnectionString* で指定した値より優先されます。

開いている **Connection** オブジェクトに対する操作が完了したら、[Close](close-method-ado.md) メソッドを使用して関連するすべてのシステム リソースを解放します。オブジェクトを閉じても、オブジェクトはメモリから削除されません。オブジェクトのプロパティ設定を変更し、**Open** メソッドを使用して、後で再度開くことができます。オブジェクトをメモリから完全に削除するには、オブジェクト変数に *Nothing* を設定します。

**リモート データ サービスの使用法**クライアント側の**接続**オブジェクトを使用する場合は、**接続**オブジェクトの[レコード セット](recordset-object-ado.md)が開かれるまで、 **Open**メソッドは実際には、サーバーへの接続を確立されません。


> [!NOTE]
> [!メモ] http 体系を使用している URL は、[Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) を自動的に呼び出します。 詳細については、[絶対と相対 Url](absolute-and-relative-urls.md)を参照してください。


