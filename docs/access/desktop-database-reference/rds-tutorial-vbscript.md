---
title: RDS チュートリアル (VBScript)
TOCTitle: RDS tutorial (VBScript)
ms:assetid: 7a6596fd-00b9-a637-7d00-fb55a621305f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249506(v=office.15)
ms:contentKeyID: 48545792
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c1c6b42d9560a30b45fb777bb4fd1de4351830a4
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936295"
---
# <a name="rds-tutorial-vbscript"></a><span data-ttu-id="2dfe7-102">RDS チュートリアル (VBScript)</span><span class="sxs-lookup"><span data-stu-id="2dfe7-102">RDS tutorial (VBScript)</span></span>

<span data-ttu-id="2dfe7-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="2dfe7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2dfe7-104">これは、RDS チュートリアルでは、Microsoft Visual Basic Scripting Edition で書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="2dfe7-104">This is the RDS tutorial, written in Microsoft Visual Basic Scripting Edition.</span></span> <span data-ttu-id="2dfe7-105">このチュートリアルの目的については、 [RDS チュートリアル](chapter-12-rds-tutorial.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2dfe7-105">For a description of the purpose of this tutorial, see the [RDS tutorial](chapter-12-rds-tutorial.md).</span></span>

<span data-ttu-id="2dfe7-106">このチュートリアルでは、 [rds.DataControl](datacontrol-object-rds.md)と[rds.作成され](dataspace-object-rds.md)は、デザイン時に作成つまり、object タグで定義されています。</span><span class="sxs-lookup"><span data-stu-id="2dfe7-106">In this tutorial, [RDS.DataControl](datacontrol-object-rds.md) and [RDS.DataSpace](dataspace-object-rds.md) are created at design time; that is, they are defined with object tags.</span></span> <span data-ttu-id="2dfe7-107">また、実行時に **Server.CreateObject** メソッドを使用して作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="2dfe7-107">Alternatively, they could be created at run time with the **Server.CreateObject** method.</span></span> 

<span data-ttu-id="2dfe7-108">たとえば、 **RDS.DataControl** オブジェクトは次のようにして作成できます。</span><span class="sxs-lookup"><span data-stu-id="2dfe7-108">For example, the **RDS.DataControl** object could be created like this:</span></span>

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

## <a name="step-1--specify-a-server-program"></a><span data-ttu-id="2dfe7-109">手順 1: サーバー プログラムを指定する</span><span class="sxs-lookup"><span data-stu-id="2dfe7-109">Step 1 — Specify a server program</span></span>

<span data-ttu-id="2dfe7-110">VBScript では、中に Active Server Pages で利用できる VBScript の**Request.ServerVariables**メソッドにアクセスする IIS web サーバーの名前を検出できます。</span><span class="sxs-lookup"><span data-stu-id="2dfe7-110">VBScript can discover the name of the IIS web server it is running on by accessing the VBScript **Request.ServerVariables** method available to Active Server Pages:</span></span>

```vb 
 
"https://<%=Request.ServerVariables("SERVER_NAME")%>" 
```

<span data-ttu-id="2dfe7-111">ただし、このチュートリアルを使用して、想像上のサーバーでは、「通常」にします。</span><span class="sxs-lookup"><span data-stu-id="2dfe7-111">However, for this tutorial, use the imaginary server, "yourServer."</span></span>

> [!NOTE]
> <P><span data-ttu-id="2dfe7-p103">[!メモ] <STRONG>ByRef</STRONG> 引数のデータ型に注意してください。VBScript では変数の型指定はできないため、常にバリアント型 (Variant) を渡す必要があります。HTTP を使用している場合は、RDS によってバリアント型 (Variant) をメソッドに渡すことができます。これを <STRONG>RDS.DataSpace</STRONG> オブジェクトの <A href="createobject-method-rds.md">CreateObject</A> メソッドで呼び出すと、非バリアント型となります。DCOM またはインプロセス サーバーを使用している場合は、クライアント側とサーバー側のパラメーター型を一致させてください。一致しない場合は、"型が一致しません。" エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="2dfe7-p103">Pay attention to the data type of <STRONG>ByRef</STRONG> arguments. VBScript does not let you specify the variable type, so you must always pass a Variant. When using HTTP, RDS will allow you to pass a Variant to a method that expects a non-Variant if you invoke it with the <STRONG>RDS.DataSpace</STRONG> object <A href="createobject-method-rds.md">CreateObject</A> method. When using DCOM or an in-process server, match the parameter types on the client and server sides or you will receive a "Type Mismatch" error.</span></span></P>

```vb
 
Set DF1 = DS1.CreateObject("RDSServer.DataFactory", "https://yourServer") 
```

## <a name="step-2a--invoke-the-server-program-with-rdsdatacontrol"></a><span data-ttu-id="2dfe7-116">手順 2a: RDS.DataControl を使用してサーバー プログラムを呼び出す</span><span class="sxs-lookup"><span data-stu-id="2dfe7-116">Step 2a — Invoke the server program with RDS.DataControl</span></span>

<span data-ttu-id="2dfe7-117">次の例は、 **RDS.DataControl** の既定の動作が指定されたクエリの実行であることを単に示したものです。</span><span class="sxs-lookup"><span data-stu-id="2dfe7-117">This example is merely a comment demonstrating that the default behavior of the **RDS.DataControl** is to perform the specified query.</span></span>

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

## <a name="step-2b--invoke-the-server-program-with-rdsserverdatafactory"></a><span data-ttu-id="2dfe7-118">手順 2b: RDSServer.DataFactory を使用してサーバー プログラムを呼び出す</span><span class="sxs-lookup"><span data-stu-id="2dfe7-118">Step 2b — Invoke the server program with RDSServer.DataFactory</span></span>

## <a name="step-3--server-obtains-a-recordset"></a><span data-ttu-id="2dfe7-119">手順 3: サーバーが Recordset を取得する</span><span class="sxs-lookup"><span data-stu-id="2dfe7-119">Step 3 — Server obtains a Recordset</span></span>

## <a name="step-4--server-returns-the-recordset"></a><span data-ttu-id="2dfe7-120">手順 4: サーバーが Recordset を返す</span><span class="sxs-lookup"><span data-stu-id="2dfe7-120">Step 4 — Server returns the Recordset</span></span>

```vb
 
Set RS = DF1.Query("DSN=Pubs;", "SELECT * FROM Authors") 
```

## <a name="step-5--datacontrol-is-made-usable-by-visual-controls"></a><span data-ttu-id="2dfe7-121">手順 5: ビジュアル コントロールによって DataControl を利用可能にする</span><span class="sxs-lookup"><span data-stu-id="2dfe7-121">Step 5 — DataControl is made usable by visual controls</span></span>

```vb
 
' Assign the returned recordset to the DataControl. 
 
DC1.SourceRecordset = RS 
```

## <a name="step-6a--changes-are-sent-to-the-server-with-rdsdatacontrol"></a><span data-ttu-id="2dfe7-122">手順 6: 変更が送信されてサーバーに rds.DataControl \*</span><span class="sxs-lookup"><span data-stu-id="2dfe7-122">Step 6a — Changes are sent to the server with RDS.DataControl\*</span></span>

<span data-ttu-id="2dfe7-123">次の例は、 **RDS.DataControl** がどのようにして更新を行うかを単に示したものです。</span><span class="sxs-lookup"><span data-stu-id="2dfe7-123">This example is merely a comment demonstrating how the **RDS.DataControl** performs updates.</span></span>

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

## <a name="step-6b--changes-are-sent-to-the-server-with-rdsserverdatafactory"></a><span data-ttu-id="2dfe7-124">手順 6b: RDSServer.DataFactory を使用してサーバーに変更を送信する</span><span class="sxs-lookup"><span data-stu-id="2dfe7-124">Step 6b — Changes are sent to the server with RDSServer.DataFactory</span></span>

```vb
 
DF.SubmitChanges"DSN=Pubs", RS 
 
End Sub 
</SCRIPT> 
</BODY> 
</HTML> 
```

<span data-ttu-id="2dfe7-125">**これでチュートリアルを終了します。**</span><span class="sxs-lookup"><span data-stu-id="2dfe7-125">**This is the end of the tutorial.**</span></span>

