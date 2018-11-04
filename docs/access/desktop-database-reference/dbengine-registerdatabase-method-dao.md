---
title: DBEngine.RegisterDatabase メソッド (DAO)
TOCTitle: RegisterDatabase Method
ms:assetid: ed87a694-2c89-0a78-5d8b-0cc7e09fadff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836347(v=office.15)
ms:contentKeyID: 48548541
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052938
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 8310f695bdcf229e61e09bce6c0846f9520c0fc6
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949867"
---
# <a name="dbengineregisterdatabase-method-dao"></a>DBEngine.RegisterDatabase メソッド (DAO)

**適用されます**Access 2013、Office 2013。

ODBC データ ソースの接続情報を Windows レジストリに追加します。ODBC ドライバーでは、セッション中に ODBC データ ソースが開かれるときに、接続情報が必要になります。

## <a name="syntax"></a>構文

*式*です。RegisterDatabase (***Dsn******ドライバー***、***サイレント***、***属性***)

*式***DBEngine**オブジェクトを表す変数です。

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
<th><p>必須/オプション</p></th>
<th><p>データ型</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Dsn</em></p></td>
<td><p>必須</p></td>
<td><p><strong>文字列型 (String)</strong></p></td>
<td><p><strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong> メソッドで使用される名前です。データ ソースに関する説明的な情報を指します。たとえば、データ ソースが ODBC リモート データベースである場合は、サーバー名などを指定します。</p></td>
</tr>
<tr class="even">
<td><p><em>ドライバー</em></p></td>
<td><p>必須</p></td>
<td><p><strong>文字列型 (String)</strong></p></td>
<td><p>ODBC ドライバーの名前です。ODBC ドライバーの DLL ファイルの名前ではありません。</p></td>
</tr>
<tr class="odd">
<td><p><em>サイレント</em></p></td>
<td><p>必須</p></td>
<td><p><strong>ブール型 (Boolean)</strong></p></td>
<td><p><strong>True の</strong>場合、ドライバー固有の情報の入力を求める ODBC ドライバー ダイアログ ボックスを表示したくないです。または、 <strong>false を指定</strong>する場合は、ODBC ドライバーのダイアログ ボックスを表示します。 場合<strong>はサイレント</strong>、属性には、必要なすべてのドライバー固有の情報が含まれている必要があります、またはダイアログ ボックスが表示されますか。</p></td>
</tr>
<tr class="even">
<td><p><em>Attributes</em></p></td>
<td><p>必須</p></td>
<td><p><strong>文字列型 (String)</strong></p></td>
<td><p>Windows レジストリに追加するキーワードの一覧です。キーワードは、改行で区切られた文字列として指定します。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

**RegisterDatabase** メソッドを使用した時点で、データベースが既に Windows レジストリに登録されている (接続情報が既に追加されている) 場合は、その接続情報が更新されます。

**RegisterDatabase** メソッドがなんらかの理由で失敗すると、Windows レジストリは変更されず、エラーが発生します。

SQL Server など ODBC ドライバーの詳細については、ドライバーに付属のヘルプ ファイルを参照してください。

## <a name="example"></a>例

次の例では、 **RegisterDatabase** メソッドを使用して、Publishers という名前の Microsoft SQL Server データ ソースを Windows レジストリに登録します。

```vb 
Sub RegisterDatabaseX() 
 
 Dim dbsRegister As Database 
 Dim strDescription As String 
 Dim strAttributes As String 
 Dim errLoop As Error 
 
 ' Build keywords string. 
 strDescription = InputBox( "Enter a description " & _ 
 "for the database to be registered.") 
 strAttributes = "Database=pubs" & _ 
 vbCr & "Description=" & strDescription & _ 
 vbCr & "OemToAnsi=No" & _ 
 vbCr & "Server=Server1" 
 
 ' Update Windows Registry. 
 On Error GoTo Err_Register 
 DBEngine.RegisterDatabase "Publishers", "SQL Server", _ 
 True, strAttributes 
 On Error GoTo 0 
 
 MsgBox "Use regedit.exe to view changes: " & _ 
 "HKEY_CURRENT_USER\" & _ 
 "Software\ODBC\ODBC.INI" 
 
 Exit Sub 
 
Err_Register: 
 
 ' Notify user of any errors that result from 
 ' the invalid data. 
 If DBEngine.Errors.Count > 0 Then 
 For Each errLoop In DBEngine.Errors 
 MsgBox "Error number: " & errLoop.Number & _ 
 vbCr & errLoop.Description 
 Next errLoop 
 End If 
 
 Resume Next 
 
End Sub 
 
```

