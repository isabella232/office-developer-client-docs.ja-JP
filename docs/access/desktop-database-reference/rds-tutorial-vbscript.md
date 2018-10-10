---
title: RDS チュートリアル (VBScript)
TOCTitle: RDS Tutorial (VBScript)
ms:assetid: 7a6596fd-00b9-a637-7d00-fb55a621305f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249506(v=office.15)
ms:contentKeyID: 48545792
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8d8bc6d0bb2b2f5402a10a690bb0003170357b21
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478004"
---
# <a name="rds-tutorial-vbscript"></a><span data-ttu-id="9f4b6-102">RDS チュートリアル (VBScript)</span><span class="sxs-lookup"><span data-stu-id="9f4b6-102">RDS Tutorial (VBScript)</span></span>


<span data-ttu-id="9f4b6-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="9f4b6-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9f4b6-p101">これは、Microsoft Visual Basic Scripting Edition でコーディングされた RDS チュートリアルです。このチュートリアルの目的については、「[12 章: RDS チュートリアル](chapter-12-rds-tutorial.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9f4b6-p101">This is the RDS Tutorial, written in Microsoft Visual Basic Scripting Edition. For a description of the purpose of this tutorial, see the [RDS Tutorial](chapter-12-rds-tutorial.md).</span></span>

<span data-ttu-id="9f4b6-106">このチュートリアルでは、 [rds.DataControl](datacontrol-object-rds.md)と[rds.インスタンス](dataspace-object-rds.md)の設計時に作成される-は、次のように、object タグで定義されている: です。</span><span class="sxs-lookup"><span data-stu-id="9f4b6-106">In this tutorial, [RDS.DataControl](datacontrol-object-rds.md) and [RDS.DataSpace](dataspace-object-rds.md) are created at design time — that is, they are defined with object tags, like this: .</span></span> <span data-ttu-id="9f4b6-107">また、実行時に **Server.CreateObject** メソッドを使用して作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="9f4b6-107">Alternatively, they could be created at run time with the **Server.CreateObject** method.</span></span> <span data-ttu-id="9f4b6-108">たとえば、 **RDS.DataControl** オブジェクトは次のようにして作成できます。</span><span class="sxs-lookup"><span data-stu-id="9f4b6-108">For example, the **RDS.DataControl** object could be created like this:</span></span>

```vb
    Set DC = Server.CreateObject("RDS.DataControl") 
     <!-- RDS.DataControl --> 
     <OBJECT 
     ID="DC1" CLASSID="CLSID:BD96C556-65A3-11D0-983A-00C04FC29E33"> 
     </OBJECT> 
     
     <!-- RDS.DataSpace --> 
     <OBJECT 
     ID="DS1" WIDTH=1 HEIGHT=1 
     CLASSID="CLSID:BD96C556-65A3-11D0-983A-00C04FC29E36"> 
     </OBJECT> 
     
     <SCRIPT LANGUAGE="VBScript"> 
     
     Sub RDSTutorial() 
     Dim DF1 
```

<span data-ttu-id="9f4b6-109">**手順 1: サーバー プログラムを指定する**</span><span class="sxs-lookup"><span data-stu-id="9f4b6-109">**Step 1 — Specify a server program**</span></span>

<span data-ttu-id="9f4b6-110">VBScript は、Active Server Pages で利用できる VBScript の **Request.ServerVariables** メソッドにアクセスすることにより、VBScript が動作している IIS Web サーバーの名前を検出できます。</span><span class="sxs-lookup"><span data-stu-id="9f4b6-110">VBScript can discover the name of the IIS Web server it is running on by accessing the VBScript **Request.ServerVariables** method available to Active Server Pages:</span></span>

```vb 
 
"https://<%=Request.ServerVariables("SERVER_NAME")%>" 
```

<span data-ttu-id="9f4b6-111">ただし、このチュートリアルでは架空のサーバー名 "yourServer" を使用します。</span><span class="sxs-lookup"><span data-stu-id="9f4b6-111">However, for this tutorial, use the imaginary server, "yourServer".</span></span>


> [!NOTE]
> <P><span data-ttu-id="9f4b6-p103">[!メモ] <STRONG>ByRef</STRONG> 引数のデータ型に注意してください。VBScript では変数の型指定はできないため、常にバリアント型 (Variant) を渡す必要があります。HTTP を使用している場合は、RDS によってバリアント型 (Variant) をメソッドに渡すことができます。これを <STRONG>RDS.DataSpace</STRONG> オブジェクトの <A href="createobject-method-rds.md">CreateObject</A> メソッドで呼び出すと、非バリアント型となります。DCOM またはインプロセス サーバーを使用している場合は、クライアント側とサーバー側のパラメーター型を一致させてください。一致しない場合は、"型が一致しません。" エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="9f4b6-p103">Pay attention to the data type of <STRONG>ByRef</STRONG> arguments. VBScript does not let you specify the variable type, so you must always pass a Variant. When using HTTP, RDS will allow you to pass a Variant to a method that expects a non-Variant if you invoke it with the <STRONG>RDS.DataSpace</STRONG> object <A href="createobject-method-rds.md">CreateObject</A> method. When using DCOM or an in-process server, match the parameter types on the client and server sides or you will receive a "Type Mismatch" error.</span></span></P>

```vb
 
Set DF1 = DS1.CreateObject("RDSServer.DataFactory", "https://yourServer") 
```

<span data-ttu-id="9f4b6-116">**手順 2a: RDS.DataControl を使用してサーバー プログラムを呼び出す**</span><span class="sxs-lookup"><span data-stu-id="9f4b6-116">**Step 2a — Invoke the server program with RDS.DataControl**</span></span>

<span data-ttu-id="9f4b6-117">次の例は、 **RDS.DataControl** の既定の動作が指定されたクエリの実行であることを単に示したものです。</span><span class="sxs-lookup"><span data-stu-id="9f4b6-117">This example is merely a comment demonstrating that the default behavior of the **RDS.DataControl** is to perform the specified query.</span></span>

```vb
 
<OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DC1"> 
 <PARAM NAME="SQL" VALUE="SELECT * FROM Authors"> 
 <PARAM NAME="Connect" VALUE="DSN=Pubs;"> 
 <PARAM NAME="Server" VALUE="https://yourServer/"> 
</OBJECT> 
... 
<SCRIPT LANGUAGE="VBScript"> 
 
Sub RDSTutorial2A() 
 Dim RS 
 DC1.Refresh 
 Set RS = DC1.Recordset 
... 
```

<span data-ttu-id="9f4b6-118">**手順 2b: RDSServer.DataFactory を使用してサーバー プログラムを呼び出す**</span><span class="sxs-lookup"><span data-stu-id="9f4b6-118">**Step 2b — Invoke the server program with RDSServer.DataFactory**</span></span>

<span data-ttu-id="9f4b6-119">**手順 3: サーバーが Recordset を取得する**</span><span class="sxs-lookup"><span data-stu-id="9f4b6-119">**Step 3 — Server obtains a Recordset**</span></span>

<span data-ttu-id="9f4b6-120">**手順 4: サーバーが Recordset を返す**</span><span class="sxs-lookup"><span data-stu-id="9f4b6-120">**Step 4 — Server returns the Recordset**</span></span>

```vb
 
Set RS = DF1.Query("DSN=Pubs;", "SELECT * FROM Authors") 
```

<span data-ttu-id="9f4b6-121">**手順 5: ビジュアル コントロールによって DataControl を利用可能にする**</span><span class="sxs-lookup"><span data-stu-id="9f4b6-121">**Step 5 — DataControl is made usable by visual controls**</span></span>

```vb
 
' Assign the returned recordset to the DataControl. 
 
DC1.SourceRecordset = RS 
```

<span data-ttu-id="9f4b6-122">**手順 6a: RDS.DataControl を使用してサーバーに変更を送信する**</span><span class="sxs-lookup"><span data-stu-id="9f4b6-122">**Step 6a — Changes are sent to the server with RDS.DataControl**</span></span>

<span data-ttu-id="9f4b6-123">次の例は、 **RDS.DataControl** がどのようにして更新を行うかを単に示したものです。</span><span class="sxs-lookup"><span data-stu-id="9f4b6-123">This example is merely a comment demonstrating how the **RDS.DataControl** performs updates.</span></span>

```vb
 
<OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DC1"> 
 <PARAM NAME="SQL" VALUE="SELECT * FROM Authors"> 
 <PARAM NAME="Connect" VALUE="DSN=Pubs;"> 
 <PARAM NAME="Server" VALUE="https://yourServer/"> 
</OBJECT> 
... 
<SCRIPT LANGUAGE="VBScript"> 
 
Sub RDSTutorial6A() 
Dim RS 
DC1.Refresh 
... 
Set RS = DC1.Recordset 
' Edit the Recordset object... 
' The SERVER and CONNECT properties are already set from Step 2A. 
Set DC1.SourceRecordset = RS 
... 
DC1.SubmitChanges 
```

<span data-ttu-id="9f4b6-124">**手順 6b: RDSServer.DataFactory を使用してサーバーに変更を送信する**</span><span class="sxs-lookup"><span data-stu-id="9f4b6-124">**Step 6b — Changes are sent to the server with RDSServer.DataFactory**</span></span>

```vb
 
DF.SubmitChanges"DSN=Pubs", RS 
 
End Sub 
</SCRIPT> 
</BODY> 
</HTML> 
```

<span data-ttu-id="9f4b6-125">**これでチュートリアルを終了します。**</span><span class="sxs-lookup"><span data-stu-id="9f4b6-125">**This is the end of the tutorial.**</span></span>

