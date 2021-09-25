---
title: VBScript での ADO プログラミング
TOCTitle: VBScript ADO Programming
ms:assetid: 24be1c70-8813-ed98-c3e5-fb33a68e7b41
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249019(v=office.15)
ms:contentKeyID: 48543764
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 781019e44248866f6926e58bb3f75e9b044c4e4e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593307"
---
# <a name="vbscript-ado-programming"></a>VBScript ADO プログラミング


**適用先**: Access 2013、Office 2013 

## <a name="creating-an-ado-project"></a>ADO プロジェクトの作成

Microsoft Visual Basic Scripting Edition では、タイプ ライブラリをサポートしていないので、プロジェクトの ADO を参照する必要はありません。したがって、コマンド行の完全な確定などの関連付け機能はサポートしていません。また、VBScript において、既定では ADO 列挙定数を定義しません。

ただし、ADO では、VBScript 用の次の定義を納めた 2 つのインクルード ファイルを用意しています。

  - サーバー側スクリプトでは、既定で c: Program Files Common Files System ado フォルダーにインストールされている Adovbs.inc \\ \\ \\ \\ \\ を使用します。

  - クライアント側スクリプトでは、既定で c: Program Files Common Files System msdac フォルダーにインストールされている Adcvbs.inc \\ \\ \\ \\ \\ を使用します。

これらのファイルから定数定義をコピーして ASP ページに貼り付けるか、サーバー側スクリプトを実行している場合は、Adovbs.inc ファイルを Web サイトのフォルダーにコピーし、ASP ページから参照します。

```vb 
 
<!--#include File="adovbs.inc"--> 
```

## <a name="creating-ado-objects-in-vbscript"></a>VBScript における ADO オブジェクトの作成

**Dim** ステートメントでは、オブジェクトを VBScript の特定の型に割り当てることはできません。また、VBScript では、Visual Basic for Applications の **Dim** ステートメントに使用する **New** 構文もサポートしていません。代わりに、**CreateObject** 関数呼び出しを使用します。

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

VBScript のより具体的な例については、ADO のマニュアルを参照してください。 詳細については[、「Microsoft Visual Basic Scripting Edition の ADO コード例」を参照してください](ado-code-examples-in-microsoft-visual-basic-scripting-edition.md)。

## <a name="differences-between-vbscript-and-visual-basic"></a>VBScript と Visual Basic の違い

構文の使用方法を始め、VBScript で ADO を実行することは、Visual Basic で ADO を実行する場合と、さまざまな点で似ています。ただし、いくつか大きな違いもあります。

- VBScript は、さまざまな種類のデータを格納できるバリアント型 (Variant) だけをサポートしています。バリアント データ型で必要なデータを保存しても、そのデータは VBScript によってキャストされるので正しく機能します。VBScript は ADO に必要な型を認識し、値をバリアント型に変換します。

- `on error goto <label>`VBScript 内では使用できません。

- VBScript は、 **Msgbox** 、 **Date** 、および **IsNumeric** などの組み込み Visual Basic 関数をサポートしています。ただし、VBScript は Visual Basic のサブセットなので、すべての組み込み関数をサポートしているわけではありません。たとえば、VBScript は **Format** 関数とファイル入出力関数はサポートしていません。

