---
title: VBScript での ADO プログラミング
TOCTitle: VBScript ADO Programming
ms:assetid: 24be1c70-8813-ed98-c3e5-fb33a68e7b41
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249019(v=office.15)
ms:contentKeyID: 48543764
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 694580005a3d016448ea9e5e715fea236a1d93f5
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944866"
---
# <a name="vbscript-ado-programming"></a>VBScript の ADO プログラミング


**適用されます**Access 2013、Office 2013。 

## <a name="creating-an-ado-project"></a>ADO プロジェクトの作成

Microsoft Visual Basic Scripting Edition では、タイプ ライブラリをサポートしていないので、プロジェクトの ADO を参照する必要はありません。したがって、コマンド行の完全な確定などの関連付け機能はサポートしていません。また、VBScript において、既定では ADO 列挙定数を定義しません。

ただし、ADO では、VBScript 用の次の定義を納めた 2 つのインクルード ファイルを用意しています。

  - サーバー側スクリプトを使用する Adovbs.inc を装着されている c:\\Program Files\\共通ファイル\\システム\\ado\\既定のフォルダーです。

  - クライアント側スクリプトを使用する Adcvbs.inc を装着されている c:\\Program Files\\共通ファイル\\システム\\msdac\\既定のフォルダーです。

コピーし定数の定義これらのファイルからを ASP ページに貼り付けるか、サーバー側スクリプトを実行する場合 Adovbs.inc ファイル、フォルダーにコピー、web サイトとそれを次のように、ASP ページから参照します。

```vb 
 
<!--#include File="adovbs.inc"--> 
```

## <a name="creating-ado-objects-in-vbscript"></a>VBScript における ADO オブジェクトの作成

**Dim** ステートメントでは、オブジェクトを VBScript の特定の型に割り当てることはできません。また、VBScript では、Visual Basic for Applications の **Dim** ステートメントに使用する **New** 構文もサポートしていません。代わりに、 **CreateObject** 関数呼び出しを使用します。

```vb 
 
Dim Rs1 
Set Rs1 = Server.CreateObject( "ADODB.Recordset" ) 
```

## <a name="vbscript-examples"></a>VBScript の例

次のコードは、Active Server Page (ASP) ファイルにおける VBScript サーバー側プログラミングの一般的な例です。

```vb 
 
<%  @LANGUAGE="VBSCRIPT" %> 
<%  Option Explicit %> 
<!--#include File="adovbs.inc"--> 
<HTML> 
    <BODY BGCOLOR="White" topmargin="10" leftmargin="10"> 
 
    <!-- Your ASP Code goes here --> 
<% 
Dim Source 
Dim Connect 
Dim Rs1 
     
Source = "SELECT * FROM Authors" 
Connect = "Provider=sqloledb;Data Source=srv;" & _ 
    "Initial Catalog=Pubs;Integrated Security=SSPI;" 
 
Set Rs1 = Server.CreateObject( "ADODB.Recordset" ) 
Rs1.Open Source, Connect, adOpenForwardOnly 
Response.Write("Success!") 
%> 
    </BODY> 
</HTML> 
```

VBScript のより具体的な例については、ADO のマニュアルを参照してください。 詳細については、 [Microsoft Visual Basic Scripting Edition での ADO コードの例](ado-code-examples-in-microsoft-visual-basic-scripting-edition.md)を参照してください。

## <a name="differences-between-vbscript-and-visual-basic"></a>VBScript と Visual Basic の違い

構文の使用方法を始め、VBScript で ADO を実行することは、Visual Basic で ADO を実行する場合と、さまざまな点で似ています。ただし、いくつか大きな違いもあります。

- VBScript は、さまざまな種類のデータを格納できるバリアント型 (Variant) だけをサポートしています。バリアント データ型で必要なデータを保存しても、そのデータは VBScript によってキャストされるので正しく機能します。VBScript は ADO に必要な型を認識し、値をバリアント型に変換します。

- 使用することはできません`on error goto <label>`VBScript 内。

- VBScript は、 **Msgbox** 、 **Date** 、および **IsNumeric** などの組み込み Visual Basic 関数をサポートしています。ただし、VBScript は Visual Basic のサブセットなので、すべての組み込み関数をサポートしているわけではありません。たとえば、VBScript は **Format** 関数とファイル入出力関数はサポートしていません。

