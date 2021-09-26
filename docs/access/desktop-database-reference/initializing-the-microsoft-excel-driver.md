---
title: Microsoft Office Excel ドライバーの初期化
TOCTitle: Initializing the Microsoft Excel driver
ms:assetid: 06c7f823-8e74-0811-cc00-e6b32075ef11
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844939(v=office.15)
ms:contentKeyID: 48543054
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032159
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: b267e671974d63cd844d04fe93673a8123a95873
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618050"
---
# <a name="initializing-the-microsoft-excel-driver"></a>Microsoft Office Excel ドライバーの初期化

**適用対象**: Excel 2016 |Access 2016 |Access 2013 |Office 2013 |Excel 2013 |Officeビジネス 向けAccess 2013 |Excel 2010 |Access 2010

Excel ドライバーをインストールすると、セットアップ プログラムは、エンジンおよび ISAM Formats サブキーの Windows レジストリに一連の既定値を書き込みます。 これらの設定は直接変更する必要があります。これらの設定を追加、削除、または変更するには、アプリケーションのセットアップ プログラムを使用します。 次のセクションでは、データベース ドライバーの初期化と ISAM 形式Microsoft Excel説明します。

## <a name="excel-initialization-settings"></a>Excel初期化設定

**Access Connectivity \\ Engine engine Excel \\** フォルダーには、ワークシートへの外部アクセスに使用される Aceexcl.dll ドライバーの初期化Microsoft Excelがあります。 通常、このキーのエントリの設定は次のようになっています。

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
<td><p>データ型を調べる行の数です。 データ型は、最も多いデータ型によって決められます。 同数の場合は、数値型 (Number)、通貨型 (Currency)、日付型 (Date)、テキスト型 (Text)、ブール型 (Boolean) の順に決められます。 列のデータ型に一致しないデータがある場合、そのデータは <strong>Null</strong> 値として返されます。 インポート時に、列内に複数のデータ型が混在している場合は、その列全体が ImportMixedTypes の設定に従ってキャストされます。 調べる行数の既定値は 8 です。 値の型は REG_DWORD 型です。</p></td>
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
<td><p>FirstRowHasNames</p></td>
<td><p>テーブルの 1 行目に列名があるかどうかを示すバイナリ値です。値 01 では、インポート時に列名が 1 行目に設定されます。値 00 では、1 行目に列名が含まれません。この場合、列名は F1、F2、F3、というように表示されます。既定値は 01 です。値の型は REG_BINARY 型です。</p></td>
</tr>
</tbody>
</table>

<br/>

**Access Connectivity \\ Engine engine Excel \\ 8.0** フォルダーには、次のエントリが含まれています。このエントリは 97 のMicrosoft Excelされます。

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


## <a name="using-the-typeguessrows-setting-for-excel-driver"></a>ドライバーの TypeGuessRows 設定Excelする
このドライバーを **Microsoft Excel、TypeGuessRows** レジストリ値を使用して、データ型をチェックする行の数を構成できます。 **TypeGuessRows** の値は、次のレジストリ サブキーの下に位置します。

# <a name="office-2016"></a>[Office 2016](#tab/office-2016)

MSI インストールの場合は、Office

- 64 ビット Officeの 32 ビット Windows または 64 ビット Officeの 32 ビット Windows。
    
  **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**

- 64 ビット Officeの 32 ビット Windows。

  **HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**
    
システムのクイック実行インストールOffice

- 64 ビット Officeの 32 ビット Windows または 64 ビット Officeの 32 ビット Windows。
    
  **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**

- 64 ビット Officeの 32 ビット Windows。
    
  **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Wow6432Node\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**

チェックする行の既定の数は **8 (8)** です。 **TypeGuessRows** 値を **0** (ゼロ) に設定すると、Excel Driver はデータ型の最初の 16,384 行をチェックします。 16,384 行を超える行をチェックする場合は **、TypeGuessRows** を目的の範囲に基づく値に設定します。 すべての行を確認するには **、TypeGuessRows** を 1,048,576 に設定します (この値で許可される行の最大数Excel)。
 
データ型は、検出されたデータの種類の最大数によって決まります。 タイがある場合、データ型は次の順序で決定されます。

- 番号
- 通貨
- 日付
- テキスト
- ブール型

列の推測されたデータ型と一致しないデータが検出された場合、そのデータは Null 値として **返** されます。 インポート中に、列にデータ型が混在している場合、列全体が **ImportMixedTypes** 設定で設定されたデータ型にキャストされます。

# <a name="office-2013"></a>[Office 2013](#tab/office-2013)

64 ビット Officeの 32 ビット Windows または 64 ビット Officeの 32 ビット Windows。

**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**

64 ビット Officeの 32 ビット Windows。

**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**

チェックする行の既定の数は **8 (8)** です。 **TypeGuessRows** 値を **0** (ゼロ) に設定すると、Excel Driver はデータ型の最初の 16,384 行をチェックします。 16,384 行を超える行をチェックする場合は **、TypeGuessRows** を目的の範囲に基づく値に設定します。 すべての行を確認するには **、TypeGuessRows** を 1,048,576 に設定します (この値で許可される行の最大数Excel)。
 
データ型は、検出されたデータの種類の最大数によって決まります。 タイがある場合、データ型は次の順序で決定されます。

- 番号
- 通貨
- 日付
- テキスト
- ブール型

列の推測されたデータ型と一致しないデータが検出された場合、そのデータは Null 値として **返** されます。 インポート中に、列にデータ型が混在している場合、列全体が **ImportMixedTypes** 設定で設定されたデータ型にキャストされます。

# <a name="office-2010"></a>[Office 2010](#tab/office-2010)

64 ビット Officeの 32 ビット Windows または 64 ビット Officeの 32 ビット Windows。

**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**

64 ビット Officeの 32 ビット Windows。

**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**

チェックする行の既定の数は **8 (8)** です。 **TypeGuessRows** 値を **0** (ゼロ) に設定すると、Excel Driver はデータ型の最初の 16,384 行をチェックします。 16,384 行を超える行をチェックする場合は **、TypeGuessRows** を目的の範囲に基づく値に設定します。 すべての行を確認するには **、TypeGuessRows** を 1,048,576 に設定します (この値で許可される行の最大数Excel)。
 
データ型は、検出されたデータの種類の最大数によって決まります。 タイがある場合、データ型は次の順序で決定されます。

- 番号
- 通貨
- 日付
- テキスト
- ブール型

列の推測されたデータ型と一致しないデータが検出された場合、そのデータは Null 値として **返** されます。 インポート中に、列にデータ型が混在している場合、列全体が **ImportMixedTypes** 設定で設定されたデータ型にキャストされます。

---
> [!NOTE]
> [!メモ] Windows レジストリの設定を変更した場合は、新しい設定内容を有効にするために、データベース エンジンをいったん終了してから再起動する必要があります。

## <a name="see-also"></a>関連項目

- [ドライバーの TypeGuessRows 設定Excelする](https://support.office.com/en-us/article/using-the-typeguessrows-setting-for-excel-driver-6aa3e101-2a90-47ac-bf0f-7d4109a5708b?ui=en-US&rs=en-US&ad=US)

