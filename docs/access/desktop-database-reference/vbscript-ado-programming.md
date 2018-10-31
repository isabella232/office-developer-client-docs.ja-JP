---
title: VBScript での ADO プログラミング
TOCTitle: VBScript ADO Programming
ms:assetid: 24be1c70-8813-ed98-c3e5-fb33a68e7b41
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249019(v=office.15)
ms:contentKeyID: 48543764
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e94f4d313a9c43d08c9786c6f27fd49624709249
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863067"
---
# <a name="vbscript-ado-programming"></a><span data-ttu-id="c0f25-102">VBScript での ADO プログラミング</span><span class="sxs-lookup"><span data-stu-id="c0f25-102">VBScript ADO Programming</span></span>


<span data-ttu-id="c0f25-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="c0f25-103">**Applies to**: Access 2013 | Office 2013</span></span> 

## <a name="creating-an-ado-project"></a><span data-ttu-id="c0f25-104">ADO プロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="c0f25-104">Creating an ADO Project</span></span>

<span data-ttu-id="c0f25-p101">Microsoft Visual Basic Scripting Edition では、タイプ ライブラリをサポートしていないので、プロジェクトの ADO を参照する必要はありません。したがって、コマンド行の完全な確定などの関連付け機能はサポートしていません。また、VBScript において、既定では ADO 列挙定数を定義しません。</span><span class="sxs-lookup"><span data-stu-id="c0f25-p101">Microsoft Visual Basic, Scripting Edition does not support type libraries, so you do not need to reference ADO in your project. Consequently, no associated features such as command line completion are supported. Also, by default, ADO enumerated constants are not defined in VBScript.</span></span>

<span data-ttu-id="c0f25-108">ただし、ADO では、VBScript 用の次の定義を納めた 2 つのインクルード ファイルを用意しています。</span><span class="sxs-lookup"><span data-stu-id="c0f25-108">However, ADO provides you with two include files containing the following definitions to be used with VBScript:</span></span>

  - <span data-ttu-id="c0f25-109">サーバー側スクリプトを使用する Adovbs.inc を装着されている c:\\Program Files\\共通ファイル\\システム\\ado\\既定のフォルダーです。</span><span class="sxs-lookup"><span data-stu-id="c0f25-109">For server-side scripting use Adovbs.inc, which is installed in the c:\\Program Files\\Common Files\\System\\ado\\ folder by default.</span></span>

  - <span data-ttu-id="c0f25-110">クライアント側スクリプトを使用する Adcvbs.inc を装着されている c:\\Program Files\\共通ファイル\\システム\\msdac\\既定のフォルダーです。</span><span class="sxs-lookup"><span data-stu-id="c0f25-110">For client-side scripting use Adcvbs.inc, which is installed in the c:\\Program Files\\Common Files\\System\\msdac\\ folder by default.</span></span>

<span data-ttu-id="c0f25-111">コピーし定数の定義これらのファイルからを ASP ページに貼り付けるか、サーバー側スクリプトを実行する場合 Adovbs.inc ファイル、フォルダーにコピー、web サイトとそれを次のように、ASP ページから参照します。</span><span class="sxs-lookup"><span data-stu-id="c0f25-111">You can either copy and paste constant definitions from these files into your ASP pages, or, if you are doing server-side scripting, copy Adovbs.inc file to a folder on your website and referencing it from your ASP page like this:</span></span>

```vb 
 
<!--#include File="adovbs.inc"--> 
```

## <a name="creating-ado-objects-in-vbscript"></a><span data-ttu-id="c0f25-112">VBScript における ADO オブジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="c0f25-112">Creating ADO Objects in VBScript</span></span>

<span data-ttu-id="c0f25-p102">**Dim** ステートメントでは、オブジェクトを VBScript の特定の型に割り当てることはできません。また、VBScript では、Visual Basic for Applications の **Dim** ステートメントに使用する **New** 構文もサポートしていません。代わりに、 **CreateObject** 関数呼び出しを使用します。</span><span class="sxs-lookup"><span data-stu-id="c0f25-p102">You cannot use the **Dim** statement to assign objects to a specific type in VBScript. Also, VBScript does not support the **New** syntax used with the **Dim** statement in Visual Basic for Applications. You must instead use the **CreateObject** function call:</span></span>

```vb 
 
Dim Rs1 
Set Rs1 = Server.CreateObject( "ADODB.Recordset" ) 
```

## <a name="vbscript-examples"></a><span data-ttu-id="c0f25-116">VBScript の例</span><span class="sxs-lookup"><span data-stu-id="c0f25-116">VBScript Examples</span></span>

<span data-ttu-id="c0f25-117">次のコードは、Active Server Page (ASP) ファイルにおける VBScript サーバー側プログラミングの一般的な例です。</span><span class="sxs-lookup"><span data-stu-id="c0f25-117">The following code is a generic example of VBScript server-side programming in an Active Server Page (ASP) file:</span></span>

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

<span data-ttu-id="c0f25-118">VBScript のより具体的な例については、ADO のマニュアルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c0f25-118">More specific VBScript examples are included with the ADO documentation.</span></span> <span data-ttu-id="c0f25-119">詳細については、 [Microsoft Visual Basic Scripting Edition での ADO コードの例](ado-code-examples-in-microsoft-visual-basic-scripting-edition.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c0f25-119">For more information, see [ADO code examples in Microsoft Visual Basic Scripting Edition](ado-code-examples-in-microsoft-visual-basic-scripting-edition.md).</span></span>

## <a name="differences-between-vbscript-and-visual-basic"></a><span data-ttu-id="c0f25-120">VBScript と Visual Basic の違い</span><span class="sxs-lookup"><span data-stu-id="c0f25-120">Differences Between VBScript and Visual Basic</span></span>

<span data-ttu-id="c0f25-p104">構文の使用方法を始め、VBScript で ADO を実行することは、Visual Basic で ADO を実行する場合と、さまざまな点で似ています。ただし、いくつか大きな違いもあります。</span><span class="sxs-lookup"><span data-stu-id="c0f25-p104">Using ADO with VBScript is similar to using ADO with Visual Basic in many ways, including how syntax is used. However, some significant differences exist:</span></span>

- <span data-ttu-id="c0f25-p105">VBScript は、さまざまな種類のデータを格納できるバリアント型 (Variant) だけをサポートしています。バリアント データ型で必要なデータを保存しても、そのデータは VBScript によってキャストされるので正しく機能します。VBScript は ADO に必要な型を認識し、値をバリアント型に変換します。</span><span class="sxs-lookup"><span data-stu-id="c0f25-p105">VBScript supports only the Variant data type, which can hold different types of data. You can store the data you need in a Variant data type, and the data will function appropriately due to casting performed by VBScript. It recognizes the type required by ADO, and converts the value in the Variant accordingly.</span></span>

- <span data-ttu-id="c0f25-126">使用することはできません`on error goto <label>`VBScript 内。</span><span class="sxs-lookup"><span data-stu-id="c0f25-126">You cannot use `on error goto <label>` within VBScript.</span></span>

- <span data-ttu-id="c0f25-p106">VBScript は、 **Msgbox** 、 **Date** 、および **IsNumeric** などの組み込み Visual Basic 関数をサポートしています。ただし、VBScript は Visual Basic のサブセットなので、すべての組み込み関数をサポートしているわけではありません。たとえば、VBScript は **Format** 関数とファイル入出力関数はサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="c0f25-p106">VBScript supports some of the built-in Visual Basic functions such as **Msgbox**, **Date**, and **IsNumeric**. However, because VBScript is a subset of Visual Basic, not all built-in functions are supported. For example, VBScript does not support the **Format** function and the file I/O functions.</span></span>

