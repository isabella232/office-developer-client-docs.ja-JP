---
title: RDS チュートリアル (VBScript)
TOCTitle: RDS tutorial (VBScript)
ms:assetid: 7a6596fd-00b9-a637-7d00-fb55a621305f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249506(v=office.15)
ms:contentKeyID: 48545792
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 996c0adf8c883de5c73174d726cf5bd11fc42457
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996882"
---
# <a name="rds-tutorial-vbscript"></a>RDS チュートリアル (VBScript)

**適用されます**Access 2013、Office 2013。

これは、RDS チュートリアルでは、Microsoft Visual Basic Scripting Edition で書き込まれます。 このチュートリアルの目的については、 [RDS チュートリアル](chapter-12-rds-tutorial.md)を参照してください。

このチュートリアルでは、 [rds.DataControl](datacontrol-object-rds.md)と[rds.作成され](dataspace-object-rds.md)は、デザイン時に作成つまり、object タグで定義されています。 また、実行時に **Server.CreateObject** メソッドを使用して作成することもできます。 

たとえば、 **RDS.DataControl** オブジェクトは次のようにして作成できます。

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

## <a name="step-1--specify-a-server-program"></a>手順 1: サーバー プログラムを指定する

VBScript では、中に Active Server Pages で利用できる VBScript の**Request.ServerVariables**メソッドにアクセスする IIS web サーバーの名前を検出できます。

```vb 
 
"https://<%=Request.ServerVariables("SERVER_NAME")%>" 
```

ただし、このチュートリアルを使用して、想像上のサーバーでは、「通常」にします。

> [!NOTE]
> [!メモ] **ByRef** 引数のデータ型に注意してください。VBScript では変数の型指定はできないため、常にバリアント型 (Variant) を渡す必要があります。HTTP を使用している場合は、RDS によってバリアント型 (Variant) をメソッドに渡すことができます。これを **RDS.DataSpace** オブジェクトの [CreateObject](createobject-method-rds.md) メソッドで呼び出すと、非バリアント型となります。DCOM またはインプロセス サーバーを使用している場合は、クライアント側とサーバー側のパラメーター型を一致させてください。一致しない場合は、"型が一致しません。" エラーが発生します。

```vb
 
Set DF1 = DS1.CreateObject("RDSServer.DataFactory", "https://yourServer") 
```

## <a name="step-2a--invoke-the-server-program-with-rdsdatacontrol"></a>手順 2a: RDS.DataControl を使用してサーバー プログラムを呼び出す

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

## <a name="step-2b--invoke-the-server-program-with-rdsserverdatafactory"></a>手順 2b: RDSServer.DataFactory を使用してサーバー プログラムを呼び出す

## <a name="step-3--server-obtains-a-recordset"></a>手順 3: サーバーが Recordset を取得する

## <a name="step-4--server-returns-the-recordset"></a>手順 4: サーバーが Recordset を返す

```vb
 
Set RS = DF1.Query("DSN=Pubs;", "SELECT * FROM Authors") 
```

## <a name="step-5--datacontrol-is-made-usable-by-visual-controls"></a>手順 5: ビジュアル コントロールによって DataControl を利用可能にする

```vb
 
' Assign the returned recordset to the DataControl. 
 
DC1.SourceRecordset = RS 
```

## <a name="step-6a--changes-are-sent-to-the-server-with-rdsdatacontrol"></a>手順 6: 変更が送信されてサーバーに rds.DataControl *

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

## <a name="step-6b--changes-are-sent-to-the-server-with-rdsserverdatafactory"></a>手順 6b: RDSServer.DataFactory を使用してサーバーに変更を送信する

```vb
 
DF.SubmitChanges"DSN=Pubs", RS 
 
End Sub 
</SCRIPT> 
</BODY> 
</HTML> 
```

**これでチュートリアルを終了します。**

