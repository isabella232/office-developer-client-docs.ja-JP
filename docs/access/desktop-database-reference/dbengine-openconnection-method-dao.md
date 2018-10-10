---
title: DBEngine.OpenConnection メソッド (DAO)
TOCTitle: OpenConnection Method
ms:assetid: 778a581f-be42-94ee-e5c6-4cbc1843450d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196074(v=office.15)
ms:contentKeyID: 48545729
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053574
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b2c43983937ece0d24146416af354968ae2bc7f2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478321"
---
# <a name="dbengineopenconnection-method-dao"></a>DBEngine.OpenConnection メソッド (DAO)


**適用されます**Access 2013 |。Office 2013

## <a name="syntax"></a>構文

*式*です。されます (***名前***、***オプション***、***読み取り専用***、***接続***)

*式***DBEngine**オブジェクトを表す変数です。

### <a name="parameters"></a>パラメーター

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>名前</p></th>
<th><p>必須/オプション</p></th>
<th><p>データ型</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>名前</p></td>
<td><p>必須</p></td>
<td><p><strong>文字列型 (String)</strong></p></td>
<td><p>文字列式を指定します。「解説」の説明を参照してください。</p></td>
</tr>
<tr class="even">
<td><p>選択肢</p></td>
<td><p>省略可能</p></td>
<td><p><strong>バリアント型 (Variant)</strong></p></td>
<td><p>「解説」に記載されている接続のさまざまなオプションを設定します。ODBC ドライバー マネージャーは、この値に基づき、データ ソース名 (DSN)、ユーザー名、パスワードなどの接続情報の指定をユーザーに求めます。</p></td>
</tr>
<tr class="odd">
<td><p>ReadOnly</p></td>
<td><p>省略可能</p></td>
<td><p><strong>バリアント型 (Variant)</strong></p></td>
<td><p><strong>True</strong> に設定すると、接続が読み取り専用アクセスで開かれ、 <strong>False</strong> (既定値) に設定すると、読み取り/書き込みアクセスで開かれます。</p></td>
</tr>
<tr class="even">
<td><p>ブラウザでの</p></td>
<td><p>省略可能</p></td>
<td><p><strong>バリアント型 (Variant)</strong></p></td>
<td><p>ODBC 接続文字列です。 この文字列の固有の要素および構文については、 <strong><a href="connection-connect-property-dao.md">Connect</a></strong> プロパティのトピックを参照してください。 先頭に追加された&quot;ODBC;&quot;が必要です。</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>戻り値

Connection

## <a name="remarks"></a>注釈

**OpenConnection** メソッドは、ODBCDirect ワークスペースから ODBC データ ソースへの接続を確立するために使用します。 **OpenConnection** メソッドは、 **OpenDatabase** と似ていますが、同じではありません。主な違いは、 **OpenConnection** が ODBCDirect ワークスペースでしか使用できないことです。

登録済みの ODBC データ ソース名 (DSN) を指定すると、接続の引数で、引数 name は任意の有効な文字列を使用でき、**接続**オブジェクトの**Name**プロパティも提供されます。 接続の引数には、有効な DSN が含まれていない場合、名前は、 **Name**プロパティもありますが、有効な ODBC DSN を参照しなければなりません。 場合名前し、接続のどちらも、有効な DSN が含まれている ODBC ドライバ ・ マネージャーは、ユーザーに必要な接続情報を要求する (オプションの引数) を使用して設定できます。 この場合、ユーザーが指定した DSN が **Name** プロパティの値となります。

引数 options では、接続を確立するための情報の入力をユーザーに求めるかどうか、どのような場合にユーザー入力を求めるか、接続を非同期で開くかどうかを指定します。次のいずれかの定数を使用できます。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>定数</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbDriverNoPrompt</strong></p></td>
<td><p>ODBC ドライバー マネージャーは、<em>name</em> および <em>connect</em> に指定された接続文字列を使用します。情報が不足していると、実行時エラーが発生します。</p></td>
</tr>
<tr class="even">
<td><p><strong>そのまま使用</strong></p></td>
<td><p>ODBC ドライバー マネージャーは、<em>dhname</em> または <em>connect</em> で指定された関連情報を示す [<strong>接続する ODBC データ ソース</strong>] ダイアログ ボックスを開きます。接続文字列は、ユーザーがダイアログ ボックスで選択した DSN を使用して作成されますが、ユーザーが DSN を指定しなかった場合は、既定の DSN が使用されます。</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbDriverComplete</strong></p></td>
<td><p>既定値です。引数 <em>connect</em> で接続の確立に必要な情報がすべて指定されている場合、ODBC ドライバー マネージャーは <em>connect</em> で指定されている文字列を使用します。指定されていない情報がある場合は、<strong>dbDriverPrompt</strong> を指定したときと同じ動作を行います。</p></td>
</tr>
<tr class="even">
<td><p><strong>dbDriverCompleteRequired</strong></p></td>
<td><p>このオプションを指定した場合の動作は <strong>dbDriverComplete</strong> の場合と似ていますが、接続を確立するために不足している情報についてのみユーザー入力を求める点が異なります。</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbRunAsync</strong></p></td>
<td><p>メソッドを非同期で実行します。 この定数は、他の<em>オプション</em>の定数のいずれかを使用できます。</p></td>
</tr>
</tbody>
</table>


**OpenConnection** は、接続に関する情報を含む **Connection** オブジェクトを返します。 **Connection** オブジェクトは **[Database](database-object-dao.md)** オブジェクトに似ています。主な違いは、 **Database** オブジェクトは通常データベースを表すものの、Microsoft Access ワークスペースから ODBC データ ソースへの接続を表すためにも使用できることです。

