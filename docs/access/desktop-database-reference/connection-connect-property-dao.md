---
title: Connect プロパティ (DAO)
TOCTitle: Connect Property
ms:assetid: 58b514a2-91cd-7918-cba5-15d71c2457a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194335(v=office.15)
ms:contentKeyID: 48545001
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e44ce5b4acf58f3f9d9e887d0136baed64c8e227
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295927"
---
# <a name="connectionconnect-property-dao"></a>Connect プロパティ (DAO)


**適用先:** Access 2013、Office 2013

開いている接続のソースに関する情報を提供する値を設定または取得します。値の取得および設定が可能です。文字列型 (**String**) の値を使用します。

## <a name="syntax"></a>構文

*式*。結び付ける

*式***Connection**オブジェクトを表す変数を取得します。

## <a name="remarks"></a>注釈

**Connect** プロパティの設定値は、データベースの種類の指定子と 0 個以上のパラメーターで構成され、それぞれがセミコロンで区切られている文字列型 ( **String** ) の値です。 **Connect** プロパティは、必要に応じて ODBC ドライバーと特定の ISAM ドライバーに追加情報を渡します。

Microsoft Access データベース ファイルにリンクしているテーブルに対して SQL パススルー クエリを実行するには、まず、テーブルがリンクしているデータベースの **Connect** プロパティを、有効な ODBC 接続文字列に設定する必要があります。

リンク テーブルを表す **TableDef** オブジェクトの場合、 **Connect** プロパティの設定値は、1 つまたは 2 つの部分 (データベースの種類の識別子とそのデータベースへのパス) で構成され、それぞれの末尾にセミコロンが付けられています。

次の表に示すように、パスは、データベース ファイルのあるディレクトリへの完全なパスを表し、このパスの前に識別子 DATABASE= を付ける必要があります。 Microsoft Excel や Microsoft Access データベース エンジン データベースと同じように、場合によってはデータベース パスの引数に特定のファイル名を含める必要があります。

次の表は、使用できるデータベースの種類と、それに対応するデータベース識別子および **Connect** プロパティの設定値のパスを示しています。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>データベースの種類</p></th>
<th><p>識別子</p></th>
<th><p>例</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Microsoft Access データベース</p></td>
<td><p>[database];</p></td>
<td><p>drive:\path\filename</p></td>
</tr>
<tr class="even">
<td><p>dBASE III</p></td>
<td><p>dBASE III;</p></td>
<td><p>drive:\path</p></td>
</tr>
<tr class="odd">
<td><p>dBASE IV</p></td>
<td><p>dBASE IV;</p></td>
<td><p>drive:\path</p></td>
</tr>
<tr class="even">
<td><p>dBASE 5</p></td>
<td><p>dBASE 5.0;</p></td>
<td><p>drive:\path</p></td>
</tr>
<tr class="odd">
<td><p>Paradox 3.x</p></td>
<td><p>Paradox 3.x;</p></td>
<td><p>drive:\path</p></td>
</tr>
<tr class="even">
<td><p>Paradox 4.x</p></td>
<td><p>Paradox 4.x;</p></td>
<td><p>drive:\path</p></td>
</tr>
<tr class="odd">
<td><p>Paradox 5.x</p></td>
<td><p>Paradox 5.x;</p></td>
<td><p>drive:\path</p></td>
</tr>
<tr class="even">
<td><p>Microsoft Excel 3.0</p></td>
<td><p>Excel 3.0;</p></td>
<td><p>ドライブ: \ path\filename.xls</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Excel 4.0</p></td>
<td><p>Excel 4.0;</p></td>
<td><p>ドライブ: \ path\filename.xls</p></td>
</tr>
<tr class="even">
<td><p>Microsoft Excel 5.0 または Microsoft Excel 95</p></td>
<td><p>Excel 5.0;</p></td>
<td><p>ドライブ: \ path\filename.xls</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Excel 97</p></td>
<td><p>Excel 8.0;</p></td>
<td><p>ドライブ: \ path\filename.xls</p></td>
</tr>
<tr class="even">
<td><p>Lotus 1-2-3 WKS および WK1</p></td>
<td><p>Lotus WK1;</p></td>
<td><p>ドライブ: \ path\filename.wk1</p></td>
</tr>
<tr class="odd">
<td><p>Lotus 1-2-3 WK3</p></td>
<td><p>Lotus WK3;</p></td>
<td><p>ドライブ: \ path\filename.wk3</p></td>
</tr>
<tr class="even">
<td><p>Lotus 1-2-3 WK4</p></td>
<td><p>Lotus WK4;</p></td>
<td><p>ドライブ: \ path\filename.wk4</p></td>
</tr>
<tr class="odd">
<td><p>HTML インポート</p></td>
<td><p>HTML Import;</p></td>
<td><p>drive:\path\filename</p></td>
</tr>
<tr class="even">
<td><p>HTML エクスポート</p></td>
<td><p>HTML Export;</p></td>
<td><p>drive:\path</p></td>
</tr>
<tr class="odd">
<td><p>テキスト</p></td>
<td><p>Text;</p></td>
<td><p>drive:\path</p></td>
</tr>
<tr class="even">
<td><p>ODBC</p></td>
<td><p>ODBC; DATABASE=データベース; UID=ユーザー; PWD=パスワード; DSN= データソース名; [LOGINTIMEOUT=秒;]</p></td>
<td><p>なし</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Exchange</p></td>
<td><p>Exchange 4.0MAPILEVEL = folderpath、[TABLETYPE = {0 | 1}];[profile = profile;][PWD = password;][database = database;]</p></td>
<td><p>drive:\path\filename</p></td>
</tr>
</tbody>
</table>


HTML Export;

必要なパスワードが **Connect** プロパティ設定で指定されていない場合、ODBC ドライバーがテーブルに最初にアクセスし、再度接続が閉じた後で再確立されると、ログイン ダイアログ ボックスが表示されます。

Microsoft Exchange のデータの場合、必要な MAPILEVEL キーを、完全に解決されたフォルダー パス ("Mailbox - Pat SmithIAlpha/Today" など) に設定する必要があります。パスには、テーブルとして開かれるフォルダーの名前は含まれません。代わりに、そのフォルダーの名前は、**CreateTable** メソッドの引数 name として指定します。TABLETYPE キーは "0" (既定値) または "1" に設定します。"0" を設定するとフォルダーが開き、"1" に設定するとアドレス帳が開きます。PROFILE キーは、既定では現在使用中のプロファイルに設定されます。

Micorosoft Access データベースのベース テーブルの場合、**Connect** プロパティ設定は長さ 0 の文字列 ("") です。

**Database** オブジェクトの **Connect** プロパティを設定するには、 **OpenDatabase** メソッドに引数 source を指定します。設定を確認すると、データベースの種類、ユーザー ID、パスワード、または ODBC データ ソースを確かめることができます。

Microsoft Access ワークスペースの **QueryDef** オブジェクトの場合、 **Connect** プロパティを ReturnsRecords プロパティと共に使用すると、ODBC SQL パススルー クエリを作成できます。 接続文字列の databasetype は "ODBC;" で、文字列の残りの部分には、リモート データへのアクセスに使用される ODBC ドライバーに固有の情報が含まれます。 詳細については、ODBC ドライバーのマニュアルを参照してください。


> [!NOTE]
> - 先に **Connect** プロパティを設定してから、 **ReturnsRecords** プロパティを設定する必要があります。
> - アクセスするデータベース サーバーがインストールされているコンピューターに対するアクセス権限を持っている必要があります。


