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
ms.localizationpriority: medium
ms.openlocfilehash: 61014716b78af9cbfcd2b7c24e131cbd63c89095
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597458"
---
# <a name="dbengineopenconnection-method-dao"></a>DBEngine.OpenConnection メソッド (DAO)

**適用先**: Access 2013、Office 2013

## <a name="syntax"></a>構文

*式*.OpenConnection(***Name** _, _*_Options_*_, _*_ReadOnly_*_,__*_ Connect **)

*式* **DBEngine** オブジェクトを表す変数です。

## <a name="parameters"></a>パラメーター

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
<th><p>必須かどうか</p></th>
<th><p>データ型</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>名前</em></p></td>
<td><p>必須</p></td>
<td><p><strong>String</strong></p></td>
<td><p>文字列式を指定します。「解説」の説明を参照してください。</p></td>
</tr>
<tr class="even">
<td><p><em>オプション</em></p></td>
<td><p>省略可能</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>「解説」に記載されている接続のさまざまなオプションを設定します。ODBC ドライバー マネージャーは、この値に基づき、データ ソース名 (DSN)、ユーザー名、パスワードなどの接続情報の指定をユーザーに求めます。</p></td>
</tr>
<tr class="odd">
<td><p><em>ReadOnly</em></p></td>
<td><p>省略可能</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>True</strong> に設定すると、接続が読み取り専用アクセスで開かれ、 <strong>False</strong> (既定値) に設定すると、読み取り/書き込みアクセスで開かれます。</p></td>
</tr>
<tr class="even">
<td><p><em>Connect</em></p></td>
<td><p>省略可能</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>ODBC 接続文字列です。 この文字列の固有の要素および構文については、 <strong><a href="connection-connect-property-dao.md">Connect</a></strong> プロパティのトピックを参照してください。 前に追加された &quot; ODBC が &quot; 必要です。</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>戻り値

Connection

## <a name="remarks"></a>注釈

**OpenConnection** メソッドは、ODBCDirect ワークスペースから ODBC データ ソースへの接続を確立するために使用します。**OpenConnection** メソッドは、**OpenDatabase** と似ていますが、同じではありません。主な違いは、**OpenConnection** が ODBCDirect ワークスペースでしか使用できないことです。

connect 引数に登録済みの ODBC データ ソース名 (DSN) を指定した場合、name 引数には任意の有効な文字列を指定できます。**また、Connection** オブジェクトの **Name** プロパティも指定します。 有効な DSN が connect 引数に含まれていない場合、name は有効な ODBC DSN を参照する必要があります。これは Name プロパティにも **指定** されます。 名前も接続も有効な DSN が含まれている場合は、ODBC ドライバー マネージャーを (options 引数を使用して) 設定して、必要な接続情報をユーザーに要求できます。 この場合、ユーザーが指定した DSN が **Name** プロパティの値となります。

options 引数は、ユーザーに接続の確立を求めるメッセージを表示するかどうか、および接続を非同期的に開くかどうかを決定します。 次のいずれかの定数を使用できます。

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
<td><p><strong>dbDriverPrompt</strong></p></td>
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
<td><p>メソッドを非同期で実行します。この定数は、<em>options</em> で他の任意の定数と共に使用できます。</p></td>
</tr>
</tbody>
</table>


**OpenConnection** は、接続に関する情報を含む **Connection** オブジェクトを返します。 **Connection** オブジェクトは **[Database](database-object-dao.md)** オブジェクトに似ています。主な違いは、 **Database** オブジェクトは通常データベースを表すものの、Microsoft Access ワークスペースから ODBC データ ソースへの接続を表すためにも使用できることです。

