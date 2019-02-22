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
localization_priority: Normal
ms.openlocfilehash: 2fe59f34c04314f70117b3bc7f08d78c2d23ae6d
ms.sourcegitcommit: 62228a65109a9543cd223dfbf326dbf1af256748
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/22/2019
ms.locfileid: "30179664"
---
# <a name="initializing-the-microsoft-excel-driver"></a>Microsoft Office Excel ドライバーの初期化

**適用**対象: Access 2013 |Office 2013

Excel ドライバーをインストールすると、セットアッププログラムによって、エンジンおよび ISAM 形式のサブキーに、Windows レジストリに既定値のセットが書き込まれます。 これらの設定は直接変更しないでください。アプリケーションのセットアッププログラムを使用して、これらの設定を追加、削除、または変更します。 次のセクションでは、Microsoft Excel データベースドライバーの初期化と ISAM 形式の設定について説明します。

## <a name="excel-initialization-settings"></a>Excel の初期化設定

**access Connectivity Engine Engine\\\\Excel**フォルダーには、Microsoft excel ワークシートへの外部アクセスに使用される Aceexcl ドライバーの初期化設定が含まれています。 通常、このキーのエントリの設定は次のようになっています。

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
<td><p>データ型を確認する行の数を指定します。 データ型は、検出されたデータの種類の最大数に応じて決定されます。 が関連付けられている場合、データ型は次の順序で決定されます。数値、通貨、日付、テキスト、ブール値です。 列に対して推測されるデータ型と一致しないデータが検出された場合、そのデータは<strong>Null</strong>値として返されます。 インポート時に、列のデータ型が混在している場合は、ImportMixedTypes の設定に従って列全体がキャストされます。 チェックする既定の行数は8です。 値の型は REG_DWORD 型です。</p></td>
</tr>
<tr class="odd">
<td><p>ImportMixedTypes</p></td>
<td><p>MajorityType または Text のどちらかを設定できます。MajorityType を設定した場合、データ型が混在している列は、インポート時に最も数の多いデータ型にキャストされます。Text を設定した場合、データ型が混在している列は、インポート時にテキスト型 (Text) にキャストされます。既定値は Text です。値の型は REG_SZ 型です。</p></td>
</tr>
<tr class="even">
<td><p>append空白行</p></td>
<td><p>Microsoft Jet 3.5 または 4.0 で、新しいデータを追加する前にワークシートの末尾に付加される空行の数です。たとえば、AppendBlankRows を 4 に設定すると、Microsoft Jet データベース エンジンはワークシートの末尾に 4 つの空行を付加してから、その後にデータのある行を付加します。このエントリには、0 ～ 16 の範囲の整数値を設定します。既定値は 01 (1 行の付加) です。値の型は REG_DWORD 型です。</p></td>
</tr>
<tr class="odd">
<td><p>FirstRowHasNames</p></td>
<td><p>テーブルの 1 行目に列名があるかどうかを示すバイナリ値です。値 01 では、インポート時に列名が 1 行目に設定されます。値 00 では、1 行目に列名が含まれません。この場合、列名は F1、F2、F3、というように表示されます。既定値は 01 です。値の型は REG_BINARY 型です。</p></td>
</tr>
</tbody>
</table>

<br/>

**access Connectivity Engine Engine\\\\Excel 8.0**フォルダーには次のエントリが含まれています。これは、Microsoft Excel 97 に適用されます。

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
<td><p>exportfilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>Microsoft Excel 97-2000 (*.xls)</p></td>
</tr>
<tr class="odd">
<td><p>canlink</p></td>
<td><p>REG_BINARY</p></td>
<td><p>atl-fs-01</p></td>
</tr>
<tr class="even">
<td><p>onetableperfile</p></td>
<td><p>REG_BINARY</p></td>
<td><p>+</p></td>
</tr>
<tr class="odd">
<td><p>isamtype</p></td>
<td><p>REG_DWORD</p></td>
<td><p>1-d</p></td>
</tr>
<tr class="even">
<td><p>indexdialog</p></td>
<td><p>REG_BINARY</p></td>
<td><p>+</p></td>
</tr>
<tr class="odd">
<td><p>createdbonexport</p></td>
<td><p>REG_BINARY</p></td>
<td><p>atl-fs-01</p></td>
</tr>
<tr class="even">
<td><p>resulttextexport</p></td>
<td><p>REG_SZ</p></td>
<td><p>カレント データベースから Microsoft Excel 97 ファイルにデータをエクスポートします。既存のファイルにエクスポートする場合、ファイル内のデータは上書きされます。</p></td>
</tr>
<tr class="odd">
<td><p>supportslongnames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>atl-fs-01</p></td>
</tr>
</tbody>
</table>

## <a name="using-the-typeguessrows-setting-for-excel-driver"></a>Excel ドライバーの TypeGuessRows 設定を使用する
Microsoft Excel ドライバーを使用する場合は、 **TypeGuessRows**レジストリ値を使用して、データ型をチェックする行の数を構成できます。 **TypeGuessRows**の値は、次のレジストリサブキーの下にあります。

# <a name="office-2016taboffice-2016"></a>[Office 2016](#tab/office-2016)

Office の MSI インストールの場合

- 32ビット版の windows または64ビット版の office (64 ビット版の windows) の場合:
    
  **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**

- 32ビット版 Office 用の64ビット版の Windows の場合:

  **HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**
    
Office のクイック実行インストールの場合

- 32ビット版の windows または64ビット版の office (64 ビット版の windows) の場合:
    
  **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**

- 32ビット版 Office 用の64ビット版の Windows の場合:
    
  **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Wow6432Node\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**

チェックする既定の行数は**8** (8) です。 **TypeGuessRows**値を**0** (ゼロ) に設定すると、Excel ドライバーはデータ型の最初の16384行をチェックします。 16384を超える行数をチェックする場合は、 **TypeGuessRows**を目的の範囲に基づく値に設定します。 すべての行をチェックするには、 **TypeGuessRows**を 1048576 (Excel で許可される最大行数) に設定します。
 
データ型は、検出されたデータの種類の最大数によって決まります。 が関連付けられている場合、データ型は次の順序で決定されます。

- 数値
- 通貨
- 日付
- テキスト
- ブール値

列の予想されるデータ型と一致しないデータが検出された場合、そのデータは**Null**値として返されます。 インポート時に、列のデータ型が混在している場合は、 **ImportMixedTypes**設定によって設定されたデータ型に列全体がキャストされます。

# <a name="office-2013taboffice-2013"></a>[Office 2013](#tab/office-2013)

32ビット版の windows または64ビット版の office (64 ビット版の windows) の場合:

**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**

32ビット版 Office 用の64ビット版の Windows の場合:

**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**

チェックする既定の行数は**8** (8) です。 **TypeGuessRows**値を**0** (ゼロ) に設定すると、Excel ドライバーはデータ型の最初の16384行をチェックします。 16384を超える行数をチェックする場合は、 **TypeGuessRows**を目的の範囲に基づく値に設定します。 すべての行をチェックするには、 **TypeGuessRows**を 1048576 (Excel で許可される最大行数) に設定します。
 
データ型は、検出されたデータの種類の最大数によって決まります。 が関連付けられている場合、データ型は次の順序で決定されます。

- 数値
- 通貨
- 日付
- テキスト
- ブール値

列の予想されるデータ型と一致しないデータが検出された場合、そのデータは**Null**値として返されます。 インポート時に、列のデータ型が混在している場合は、 **ImportMixedTypes**設定によって設定されたデータ型に列全体がキャストされます。

# <a name="office-2010taboffice-2010"></a>[Office 2010](#tab/office-2010)

32ビット版の windows または64ビット版の office (64 ビット版の windows) の場合:

**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**

32ビット版 Office 用の64ビット版の Windows の場合:

**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**

チェックする既定の行数は**8** (8) です。 **TypeGuessRows**値を**0** (ゼロ) に設定すると、Excel ドライバーはデータ型の最初の16384行をチェックします。 16384を超える行数をチェックする場合は、 **TypeGuessRows**を目的の範囲に基づく値に設定します。 すべての行をチェックするには、 **TypeGuessRows**を 1048576 (Excel で許可される最大行数) に設定します。
 
データ型は、検出されたデータの種類の最大数によって決まります。 が関連付けられている場合、データ型は次の順序で決定されます。

- 数値
- 通貨
- 日付
- テキスト
- ブール値

列の予想されるデータ型と一致しないデータが検出された場合、そのデータは**Null**値として返されます。 インポート時に、列のデータ型が混在している場合は、 **ImportMixedTypes**設定によって設定されたデータ型に列全体がキャストされます。

---
> [!NOTE]
> [!メモ] Windows レジストリの設定を変更した場合は、新しい設定内容を有効にするために、データベース エンジンをいったん終了してから再起動する必要があります。

