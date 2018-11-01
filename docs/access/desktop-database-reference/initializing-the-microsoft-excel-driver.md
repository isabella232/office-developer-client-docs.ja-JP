---
title: Microsoft Office Excel ドライバーを初期化する
TOCTitle: Initializing the Microsoft Excel Driver
ms:assetid: 06c7f823-8e74-0811-cc00-e6b32075ef11
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844939(v=office.15)
ms:contentKeyID: 48543054
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032159
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f039378c619cb5c9ebe6a70ccae718f5abfdd306
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873902"
---
# <a name="initializing-the-microsoft-excel-driver"></a>Microsoft Office Excel ドライバーを初期化する


**適用されます**Access 2013 |。Office 2013

Excel ドライバーをインストールすると、セットアップ プログラムは、一連の既定値をエンジンと ISAM 形式のサブキーで、Windows レジストリに書き込みます。 これらの設定を直接変更しないでください。追加、削除、またはこれらの設定を変更するには、アプリケーションのセットアップ プログラムを使用します。 次のセクションでは、初期化し、Microsoft Excel のデータベース ドライバーの ISAM 形式の設定について説明します。

## <a name="excel-initialization-settings"></a>Excel の初期設定

**アクセス接続エンジン\\エンジン\\Excel**フォルダーには、Microsoft Excel ワークシートへの外部アクセスの使用、Aceexcl.dll のドライバーの初期設定が含まれています。 通常、このキーのエントリの設定は次のようになっています。

```vb
    win32=<path>\ Aceexcl.dll  
    
    TypeGuessRows=8 
    
    ImportMixedTypes=Text 
    
    AppendBlankRows=1 
    
    FirstRowHasNames=Yes
```

Microsoft Access データベース エンジンで使用される、Excel キーのエントリを次に示します。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>エントリ</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>win32</p></td>
<td><p>Msexcl40.dll の格納場所です。このフル パスはインストール時に決まります。値の型は REG_SZ 型です。</p></td>
</tr>
<tr class="even">
<td><p>TypeGuessRows</p></td>
<td><p>データ型を調べる行の数です。 検出されたデータの種類の最大数を指定したデータ型が決定されます。 データ型は次の順序で決定は、同順がある場合は、: 数値、通貨、日付、文字列、ブール値です。 列のデータ型に一致しないデータが検出された場合は<strong>Null</strong>値として返されます。 インポート時に [列のデータ型が混在している場合列全体は、ImportMixedTypes の設定に従ってキャストされます。 チェックする行の既定数は、8 です。 値の型は REG_DWORD 型です。</p></td>
</tr>
<tr class="odd">
<td><p>ImportMixedTypes</p></td>
<td><p>MajorityType または Text のどちらかを設定できます。MajorityType を設定した場合、データ型が混在している列は、インポート時に最も数の多いデータ型にキャストされます。Text を設定した場合、データ型が混在している列は、インポート時にテキスト型 (Text) にキャストされます。既定値は Text です。値の型は REG_SZ 型です。</p></td>
</tr>
<tr class="even">
<td><p>AppendBlankRows</p></td>
<td><p>Microsoft Jet 3.5 または 4.0 で、新しいデータを追加する前にワークシートの末尾に付加される空行の数です。たとえば、AppendBlankRows を 4 に設定すると、Microsoft Jet データベース エンジンはワークシートの末尾に 4 つの空行を付加してから、その後にデータのある行を付加します。このエントリには、0 ～ 16 の範囲の整数値を設定します。既定値は 01 (1 行の付加) です。値の型は REG_DWORD 型です。</p></td>
</tr>
<tr class="odd">
<td><p>消えて</p></td>
<td><p>テーブルの 1 行目に列名があるかどうかを示すバイナリ値です。値 01 では、インポート時に列名が 1 行目に設定されます。値 00 では、1 行目に列名が含まれません。この場合、列名は F1、F2、F3、というように表示されます。既定値は 01 です。値の型は REG_BINARY 型です。</p></td>
</tr>
</tbody>
</table>


**アクセス接続エンジン\\エンジン\\Excel 8.0**フォルダーには、Microsoft Excel 97 に適用されますが、次のエントリが含まれています。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>エントリ名</p></th>
<th><p>型</p></th>
<th><p>値</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Engine</p></td>
<td><p>REG_SZ</p></td>
<td><p>Excel</p></td>
</tr>
<tr class="even">
<td><p>ExportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>Microsoft Excel 97-2000 (*.xls)</p></td>
</tr>
<tr class="odd">
<td><p>CanLink</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
<tr class="even">
<td><p>OneTablePerFile</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>IsamType</p></td>
<td><p>REG_DWORD</p></td>
<td><p>1</p></td>
</tr>
<tr class="even">
<td><p>IndexDialog</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>CreateDBOnExport</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
<tr class="even">
<td><p>ResultTextExport</p></td>
<td><p>REG_SZ</p></td>
<td><p>カレント データベースから Microsoft Excel 97 ファイルにデータをエクスポートします。既存のファイルにエクスポートする場合、ファイル内のデータは上書きされます。</p></td>
</tr>
<tr class="odd">
<td><p>SupportsLongNames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> [!メモ] Windows レジストリの設定を変更した場合は、新しい設定内容を有効にするために、データベース エンジンをいったん終了してから再起動する必要があります。

## <a name="see-also"></a>関連項目

[Excel ドライバーで TypeGuessRows 設定を使用します。](https://support.office.com/en-us/article/using-the-typeguessrows-setting-for-excel-driver-6aa3e101-2a90-47ac-bf0f-7d4109a5708b?ui=en-US&rs=en-US&ad=US)