---
title: JScript ADO プログラミング
TOCTitle: JScript ADO programming
ms:assetid: 2254f111-e6c2-1ad7-eb65-ee0550056d89
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249002(v=office.15)
ms:contentKeyID: 48543706
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 88a84f6fa3604286ca27651cefc999c96ff41d0e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290892"
---
# <a name="jscript-ado-programming"></a><span data-ttu-id="c212a-102">JScript ADO プログラミング</span><span class="sxs-lookup"><span data-stu-id="c212a-102">JScript ADO programming</span></span>


<span data-ttu-id="c212a-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="c212a-103">**Applies to**: Access 2013, Office 2013</span></span>


## <a name="creating-an-ado-project"></a><span data-ttu-id="c212a-104">ADO プロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="c212a-104">Creating an ADO Project</span></span>

<span data-ttu-id="c212a-p101">Microsoft JScript では、タイプ ライブラリをサポートしていないので、プロジェクトの ADO を参照する必要はありません。したがって、コマンド行の完全な確定などの関連付け機能はサポートしていません。また、JScript において、既定では ADO 列挙定数を定義しません。</span><span class="sxs-lookup"><span data-stu-id="c212a-p101">Microsoft JScript does not support type libraries, so you do not need to reference ADO in your project. Consequently, no associated features such as command line completion are supported. Also, by default, ADO enumerated constants are not defined in JScript.</span></span>

<span data-ttu-id="c212a-108">ただし、ADO では JScript 用の次の定義を納めた 2 つのインクルード ファイルを用意しています。</span><span class="sxs-lookup"><span data-stu-id="c212a-108">However, ADO provides you with two include files containing the following definitions to be used with JScript:</span></span>

- <span data-ttu-id="c212a-109">サーバー側スクリプトでは adojavas.inc を使用します。これは、既定で c\\: Program\\Files Common\\Files\\System\\ ado フォルダーにインストールされます。</span><span class="sxs-lookup"><span data-stu-id="c212a-109">For server-side scripting use Adojavas.inc, which is installed in the c:\\Program Files\\Common Files\\System\\ado\\ folder by default.</span></span>

- <span data-ttu-id="c212a-110">クライアント側スクリプトでは、Adcjavas を使用します。これは、既定で\\c:\\Program Files\\Common\\Files System\\ msdac フォルダーにインストールされます。</span><span class="sxs-lookup"><span data-stu-id="c212a-110">For client-side scripting use Adcjavas.inc, which is installed in the c:\\Program Files\\Common Files\\System\\msdac\\ folder by default.</span></span>

<span data-ttu-id="c212a-111">定数定義は、これらのファイルから ASP ページにコピーして貼り付けるか、またはサーバー側スクリプトを実行している場合は、adojavas.inc ファイルを web サイトのフォルダーにコピーして、次のように asp ページから参照します。</span><span class="sxs-lookup"><span data-stu-id="c212a-111">You can either copy and paste constant definitions from these files into your ASP pages, or, if you are doing server-side scripting, copy Adojavas.inc file to a folder on your website and references it from your ASP page like this:</span></span>

```javascript  
 
<!--#include File="adojavas.inc"--> 
```

## <a name="creating-ado-objects-in-jscript"></a><span data-ttu-id="c212a-112">JScript における ADO オブジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="c212a-112">Creating ADO Objects in JScript</span></span>

<span data-ttu-id="c212a-113">**CreateObject** 関数呼び出しを使用します。</span><span class="sxs-lookup"><span data-stu-id="c212a-113">You must instead use the **CreateObject** function call:</span></span>

```javascript  
 
var Rs1; 
Rs1 = Server.CreateObject("ADODB.Recordset"); 
```

## <a name="jscript-example"></a><span data-ttu-id="c212a-114">JScript の例</span><span class="sxs-lookup"><span data-stu-id="c212a-114">JScript Example</span></span>

<span data-ttu-id="c212a-115">次のコードは、**Recordset** オブジェクトを開く Active Server Page (ASP) ファイルにおける JScript サーバー側プログラミングの一般的な例です。</span><span class="sxs-lookup"><span data-stu-id="c212a-115">The following code is a generic example of JScript server-side programming in an Active Server Page (ASP) file that opens a **Recordset** object:</span></span>

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

