---
title: JScript の ADO プログラミング
TOCTitle: JScript ADO programming
ms:assetid: 2254f111-e6c2-1ad7-eb65-ee0550056d89
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249002(v=office.15)
ms:contentKeyID: 48543706
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 114d4d80836632721f52db0c0cb27eca5ece10f6
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25943648"
---
# <a name="jscript-ado-programming"></a><span data-ttu-id="8dc49-102">JScript の ADO プログラミング</span><span class="sxs-lookup"><span data-stu-id="8dc49-102">JScript ADO programming</span></span>


<span data-ttu-id="8dc49-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="8dc49-103">**Applies to**: Access 2013, Office 2013</span></span>


## <a name="creating-an-ado-project"></a><span data-ttu-id="8dc49-104">ADO プロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="8dc49-104">Creating an ADO Project</span></span>

<span data-ttu-id="8dc49-p101">Microsoft JScript では、タイプ ライブラリをサポートしていないので、プロジェクトの ADO を参照する必要はありません。したがって、コマンド行の完全な確定などの関連付け機能はサポートしていません。また、JScript において、既定では ADO 列挙定数を定義しません。</span><span class="sxs-lookup"><span data-stu-id="8dc49-p101">Microsoft JScript does not support type libraries, so you do not need to reference ADO in your project. Consequently, no associated features such as command line completion are supported. Also, by default, ADO enumerated constants are not defined in JScript.</span></span>

<span data-ttu-id="8dc49-108">ただし、ADO では JScript 用の次の定義を納めた 2 つのインクルード ファイルを用意しています。</span><span class="sxs-lookup"><span data-stu-id="8dc49-108">However, ADO provides you with two include files containing the following definitions to be used with JScript:</span></span>

- <span data-ttu-id="8dc49-109">サーバー側スクリプトを使用する Adojavas.inc を装着されている c:\\Program Files\\共通ファイル\\システム\\ado\\既定のフォルダーです。</span><span class="sxs-lookup"><span data-stu-id="8dc49-109">For server-side scripting use Adojavas.inc, which is installed in the c:\\Program Files\\Common Files\\System\\ado\\ folder by default.</span></span>

- <span data-ttu-id="8dc49-110">C: にインストールするクライアント側スクリプトを使用する Adcjavas.inc の\\Program Files\\ファイルの一般的な\\システム\\msdac\\既定のフォルダー。</span><span class="sxs-lookup"><span data-stu-id="8dc49-110">For client-side scripting use Adcjavas.inc, which is installed in the c:\\Program Files\\Common Files\\System\\msdac\\ folder by default.</span></span>

<span data-ttu-id="8dc49-111">コピーし定数の定義これらのファイルからを ASP ページに貼り付けるか、Adojavas.inc ファイルを web サイト上のフォルダーにコピーし、次のように、ASP ページから参照、サーバー側のスクリプトを実行する場合。</span><span class="sxs-lookup"><span data-stu-id="8dc49-111">You can either copy and paste constant definitions from these files into your ASP pages, or, if you are doing server-side scripting, copy Adojavas.inc file to a folder on your website and references it from your ASP page like this:</span></span>

```javascript  
 
<!--#include File="adojavas.inc"--> 
```

## <a name="creating-ado-objects-in-jscript"></a><span data-ttu-id="8dc49-112">JScript における ADO オブジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="8dc49-112">Creating ADO Objects in JScript</span></span>

<span data-ttu-id="8dc49-113">**CreateObject** 関数呼び出しを使用します。</span><span class="sxs-lookup"><span data-stu-id="8dc49-113">You must instead use the **CreateObject** function call:</span></span>

```javascript  
 
var Rs1; 
Rs1 = Server.CreateObject("ADODB.Recordset"); 
```

## <a name="jscript-example"></a><span data-ttu-id="8dc49-114">JScript の例</span><span class="sxs-lookup"><span data-stu-id="8dc49-114">JScript Example</span></span>

<span data-ttu-id="8dc49-115">次のコードは、 **Recordset** オブジェクトを開く Active Server Page (ASP) ファイルにおける JScript サーバー側プログラミングの一般的な例です。</span><span class="sxs-lookup"><span data-stu-id="8dc49-115">The following code is a generic example of JScript server-side programming in an Active Server Page (ASP) file that opens a **Recordset** object:</span></span>

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

