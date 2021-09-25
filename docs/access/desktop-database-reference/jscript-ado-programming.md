---
title: JScript ADO プログラミング
TOCTitle: JScript ADO programming
ms:assetid: 2254f111-e6c2-1ad7-eb65-ee0550056d89
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249002(v=office.15)
ms:contentKeyID: 48543706
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 0587f2d07342d97695524859ebca10248e70d931
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562602"
---
# <a name="jscript-ado-programming"></a>JScript ADO プログラミング


**適用先:** Access 2013、Office 2013


## <a name="creating-an-ado-project"></a>ADO プロジェクトの作成

Microsoft JScript では、タイプ ライブラリをサポートしていないので、プロジェクトの ADO を参照する必要はありません。したがって、コマンド行の完全な確定などの関連付け機能はサポートしていません。また、JScript において、既定では ADO 列挙定数を定義しません。

ただし、ADO では JScript 用の次の定義を納めた 2 つのインクルード ファイルを用意しています。

- サーバー側スクリプトでは、既定で c: Program Files Common Files System ado フォルダーにインストールされている Adojavas.inc \\ \\ \\ \\ \\ を使用します。

- クライアント側スクリプトでは、既定で c: Program Files Common Files System msdac フォルダーにインストールされている Adcjavas.inc を \\ \\ \\ \\ \\ 使用します。

これらのファイルから定数定義をコピーして ASP ページに貼り付けるか、サーバー側スクリプトを実行している場合は、Adojavas.inc ファイルを Web サイトのフォルダーにコピーし、ASP ページから次のように参照します。

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

次のコードは、**Recordset** オブジェクトを開く Active Server Page (ASP) ファイルにおける JScript サーバー側プログラミングの一般的な例です。

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

