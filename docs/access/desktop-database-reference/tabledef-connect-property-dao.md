---
title: TableDef.Connect プロパティ (DAO)
TOCTitle: Connect Property
ms:assetid: 4fbb324c-a358-8fad-60f2-fb8005cf74d9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193791(v=office.15)
ms:contentKeyID: 48544782
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053064
f1_categories:
- Office.Version=v15
ms.openlocfilehash: eaedb53c8cb70746229e3f311ba5925e3b30ddef
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478050"
---
# <a name="tabledefconnect-property-dao"></a>TableDef.Connect プロパティ (DAO)


**適用されます**Access 2013 |。Office 2013

リンク テーブルに関する情報を提供する値を設定します。値の取得および設定が可能です。文字列型 ( **String** ) の値を使用します。

## <a name="syntax"></a>構文

*式*です。接続

*式***テーブル定義**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

**Connect** プロパティの設定値は、データベースの種類の指定子と 0 個以上のパラメーターで構成され、それぞれがセミコロンで区切られている文字列型 ( **String** ) の値です。 **Connect** プロパティは、必要に応じて ODBC ドライバーと特定の ISAM ドライバーに追加情報を渡します。

リンク テーブルを表す **TableDef** オブジェクトの場合、 **Connect** プロパティの設定値は、1 つまたは 2 つの部分 (データベースの種類の識別子とそのデータベースへのパス) で構成され、それぞれの末尾にセミコロンが付けられています。

次の表のパスは、データベース ファイルのあるディレクトリへの完全なパスを表し、このパスの前に識別子 DATABASE= を付ける必要があります。Microsoft Excel や Microsoft Access データベース エンジン データベースと同じように、場合によってはデータベース パスの引数に特定のファイル名を含める必要があります。

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
<td><p><ドライブ>:\<パス>\<ファイル名>.wk1</p></td>
</tr>
<tr class="even">
<td><p>dBASE III</p></td>
<td><p>dBASE III;</p></td>
<td><p><ドライブ>:\<パス></p></td>
</tr>
<tr class="odd">
<td><p>dBASE IV</p></td>
<td><p>dBASE IV;</p></td>
<td><p><ドライブ>:\<パス></p></td>
</tr>
<tr class="even">
<td><p>dBASE 5</p></td>
<td><p>dBASE 5.0;</p></td>
<td><p><ドライブ>:\<パス></p></td>
</tr>
<tr class="odd">
<td><p>Paradox 3.x</p></td>
<td><p>Paradox 3.x;</p></td>
<td><p><ドライブ>:\<パス></p></td>
</tr>
<tr class="even">
<td><p>Paradox 4.x</p></td>
<td><p>Paradox 4.x;</p></td>
<td><p><ドライブ>:\<パス></p></td>
</tr>
<tr class="odd">
<td><p>Paradox 5.x</p></td>
<td><p>Paradox 5.x;</p></td>
<td><p><ドライブ>:\<パス></p></td>
</tr>
<tr class="even">
<td><p>Microsoft Excel 3.0</p></td>
<td><p>Excel 3.0;</p></td>
<td><p><ドライブ>:\<パス>\<ファイル名.xls></p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Excel 4.0</p></td>
<td><p>Excel 4.0;</p></td>
<td><p><ドライブ>:\<パス>\<ファイル名.xls></p></td>
</tr>
<tr class="even">
<td><p>Microsoft Excel 5.0 または Microsoft Excel 95</p></td>
<td><p>Excel 5.0;</p></td>
<td><p><ドライブ>:\<パス>\<ファイル名.xls></p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Excel 97</p></td>
<td><p>Excel 8.0;</p></td>
<td><p><ドライブ>:\<パス>\<ファイル名.xls></p></td>
</tr>
<tr class="even">
<td><p>Lotus 1-2-3 WKS および WK1</p></td>
<td><p>Lotus WK1;</p></td>
<td><p><ドライブ>:\<パス>\<ファイル名.wk1></p></td>
</tr>
<tr class="odd">
<td><p>Lotus 1-2-3 WK3</p></td>
<td><p>Lotus WK3;</p></td>
<td><p><ドライブ>:\<パス>\<ファイル名.wk3></p></td>
</tr>
<tr class="even">
<td><p>Lotus 1-2-3 WK4</p></td>
<td><p>Lotus WK4;</p></td>
<td><p><ドライブ>:\<パス>\<ファイル名.wk4></p></td>
</tr>
<tr class="odd">
<td><p>HTML インポート</p></td>
<td><p>HTML Import;</p></td>
<td><p><ドライブ>:\<パス>\<ファイル名></p></td>
</tr>
<tr class="even">
<td><p>HTML エクスポート</p></td>
<td><p>HTML Export;</p></td>
<td><p><ドライブ>:\<パス></p></td>
</tr>
<tr class="odd">
<td><p>テキスト</p></td>
<td><p>Text;</p></td>
<td><p><ドライブ>:\<パス></p></td>
</tr>
<tr class="even">
<td><p>ODBC</p></td>
<td><p>ODBC; DATABASE=データベース; UID=ユーザー; PWD=パスワード; DSN= データソース名; [LOGINTIMEOUT=秒;]</p></td>
<td><p>なし</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Exchange</p></td>
<td><p>Exchange 4.0 です。MAPILEVEL = folderpath です。[TABLETYPE = {0 | 1}]。[プロファイル = プロファイル][PWD = パスワード][データベース = データベース]</p></td>
<td><p><ドライブ>:\<パス>\<ファイル名></p></td>
</tr>
</tbody>
</table>


必要なパスワードが **Connect** プロパティ設定で指定されていない場合、ODBC ドライバーがテーブルに最初にアクセスし、再度接続が閉じた後で再確立されると、ログイン ダイアログ ボックスが表示されます。

Microsoft Exchange のデータを完全に解決済みのフォルダーのパス (たとえば、「メールボックス-Pat SmithIAlpha/今日」) に必要な MAPILEVEL キーを設定してください。 パスでは、テーブルとして表示するフォルダーの名前は含まれません**CreateTable**メソッドの引数名としてそのフォルダーの名前を指定する必要があります代わりに。 TABLETYPE キーは、フォルダー (既定値) またはアドレス帳を開くには、「1」を開く「0」に設定する必要があります。 プロファイルにプロファイル キーの既定値が使用されています。

Micorosoft Access データベースのベース テーブルの場合、 **Connect** プロパティ設定は長さ 0 の文字列 ("") です。


> [!NOTE]
> <UL>
> <LI>
> <P>[!メモ] <STRONG>ReturnsRecords</STRONG> プロパティを設定する前に、 <STRONG>Connect</STRONG> プロパティを設定する必要があります。</P>
> <LI>
> <P>アクセスするデータベース サーバーがインストールされているコンピューターに対するアクセス権限を持っている必要があります。</P></LI></UL>


