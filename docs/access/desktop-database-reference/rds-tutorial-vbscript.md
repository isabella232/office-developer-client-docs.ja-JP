---
title: RDS チュートリアル (VBScript)
TOCTitle: RDS Tutorial (VBScript)
ms:assetid: 7a6596fd-00b9-a637-7d00-fb55a621305f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249506(v=office.15)
ms:contentKeyID: 48545792
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d87dc84217b716505302464825a1857fecf67669
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606823"
---
# <a name="rds-tutorial-vbscript"></a>RDS チュートリアル (VBScript)


**適用されます**Access 2013 |。Office 2013

これは、Microsoft Visual Basic Scripting Edition でコーディングされた RDS チュートリアルです。このチュートリアルの目的については、「[12 章: RDS チュートリアル](chapter-12-rds-tutorial.md)」を参照してください。

このチュートリアルでは、 [rds.DataControl](datacontrol-object-rds.md)と[rds.インスタンス](dataspace-object-rds.md)の設計時に作成される-は、次のように、object タグで定義されている: です。 また、実行時に **Server.CreateObject** メソッドを使用して作成することもできます。 たとえば、 **RDS.DataControl** オブジェクトは次のようにして作成できます。

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

**手順 1: サーバー プログラムを指定する**

<<<<<<< ヘッドの VBScript を検出中に Active Server Pages で利用できる VBScript の**Request.ServerVariables**メソッドにアクセスする IIS Web サーバーの名前: === VBScript は、IIS web の名前を検出できます中 Active Server Pages で利用できる VBScript の**Request.ServerVariables**メソッドにアクセスするサーバー:
>>>>>>> master

```vb 
 
"https://<%=Request.ServerVariables("SERVER_NAME")%>" 
```

ただし、このチュートリアルでは架空のサーバー名 "yourServer" を使用します。


> [!NOTE]
> <P>[!メモ] <STRONG>ByRef</STRONG> 引数のデータ型に注意してください。VBScript では変数の型指定はできないため、常にバリアント型 (Variant) を渡す必要があります。HTTP を使用している場合は、RDS によってバリアント型 (Variant) をメソッドに渡すことができます。これを <STRONG>RDS.DataSpace</STRONG> オブジェクトの <A href="createobject-method-rds.md">CreateObject</A> メソッドで呼び出すと、非バリアント型となります。DCOM またはインプロセス サーバーを使用している場合は、クライアント側とサーバー側のパラメーター型を一致させてください。一致しない場合は、"型が一致しません。" エラーが発生します。</P>

```vb
 
Set DF1 = DS1.CreateObject("RDSServer.DataFactory", "https://yourServer") 
```

**手順 2a: RDS.DataControl を使用してサーバー プログラムを呼び出す**

次の例は、 **RDS.DataControl** の既定の動作が指定されたクエリの実行であることを単に示したものです。

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

**手順 2b: RDSServer.DataFactory を使用してサーバー プログラムを呼び出す**

**手順 3: サーバーが Recordset を取得する**

**手順 4: サーバーが Recordset を返す**

```vb
 
Set RS = DF1.Query("DSN=Pubs;", "SELECT * FROM Authors") 
```

**手順 5: ビジュアル コントロールによって DataControl を利用可能にする**

```vb
 
' Assign the returned recordset to the DataControl. 
 
DC1.SourceRecordset = RS 
```

**手順 6a: RDS.DataControl を使用してサーバーに変更を送信する**

次の例は、 **RDS.DataControl** がどのようにして更新を行うかを単に示したものです。

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

**手順 6b: RDSServer.DataFactory を使用してサーバーに変更を送信する**

```vb
 
DF.SubmitChanges"DSN=Pubs", RS 
 
End Sub 
</SCRIPT> 
</BODY> 
</HTML> 
```

**これでチュートリアルを終了します。**

