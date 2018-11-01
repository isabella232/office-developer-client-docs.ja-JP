---
title: JScript での ADO プログラミング
TOCTitle: JScript ADO Programming
ms:assetid: 2254f111-e6c2-1ad7-eb65-ee0550056d89
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249002(v=office.15)
ms:contentKeyID: 48543706
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dd470482c8e4a2e9228247c5eea4512367ca6483
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867238"
---
# <a name="jscript-ado-programming"></a>JScript での ADO プログラミング


**適用されます**Access 2013、Office 2013。


## <a name="creating-an-ado-project"></a>ADO プロジェクトの作成

Microsoft JScript では、タイプ ライブラリをサポートしていないので、プロジェクトの ADO を参照する必要はありません。したがって、コマンド行の完全な確定などの関連付け機能はサポートしていません。また、JScript において、既定では ADO 列挙定数を定義しません。

ただし、ADO では JScript 用の次の定義を納めた 2 つのインクルード ファイルを用意しています。

- サーバー側スクリプトを使用する Adojavas.inc を装着されている c:\\Program Files\\共通ファイル\\システム\\ado\\既定のフォルダーです。

- C: にインストールするクライアント側スクリプトを使用する Adcjavas.inc の\\Program Files\\ファイルの一般的な\\システム\\msdac\\既定のフォルダー。

コピーし定数の定義これらのファイルからを ASP ページに貼り付けるか、Adojavas.inc ファイルを web サイト上のフォルダーにコピーし、次のように、ASP ページから参照、サーバー側のスクリプトを実行する場合。

```javascript  
 
<!--#include File="adojavas.inc"--> 
```

## <a name="creating-ado-objects-in-jscript"></a>JScript における ADO オブジェクトの作成

**CreateObject** 関数呼び出しを使用します。

```javascript  
 
var Rs1; 
Rs1 = Server.CreateObject("ADODB.Recordset"); 
```

## <a name="jscript-example"></a>JScript の例

次のコードは、 **Recordset** オブジェクトを開く Active Server Page (ASP) ファイルにおける JScript サーバー側プログラミングの一般的な例です。

```javascript 
 
<%  @LANGUAGE="JScript" %> 
<!--#include File="adojavas.inc"--> 
<HTML> 
<BODY BGCOLOR="White" topmargin="10" leftmargin="10"> 
<% 
var Source = "SELECT * FROM Authors"; 
var Connect =  "Provider=sqloledb;Data Source=srv;" + 
    "Initial Catalog=Pubs;Integrated Security=SSPI;" 
var Rs1 = Server.CreateObject( "ADODB.Recordset.2.5" ); 
Rs1.Open(Source,Connect,adOpenForwardOnly); 
Response.Write("Success!"); 
%> 
</BODY> 
</HTML> 
```

