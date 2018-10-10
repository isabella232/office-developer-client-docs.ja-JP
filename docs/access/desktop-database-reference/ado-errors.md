---
title: ActiveX データ オブジェクト (ADO) エラー
TOCTitle: ADO Errors
ms:assetid: 02fcf563-ce2d-9ef7-b8ae-2795f667335a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248796(v=office.15)
ms:contentKeyID: 48542972
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ee87da91086a010066ba94b294955eebdff7b636
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476627"
---
# <a name="ado-errors"></a>ADO エラー一覧


**適用されます**Access 2013 |。Office 2013

ADO エラーは、実行時エラーとしてプログラムに報告されます。 使用しているプログラミング言語のエラー トラッピング機構を使用すると、これらのエラーをトラッピングして処理できます。 たとえば、Visual Basic では、 **On Error** ステートメントを使用します。 Visual J++ では、 **try-catch** ブロックを使用します。 Visual C++ では、ADO ライブラリへのアクセス方法によって操作が異なります。 \#のインポートは、 **try-catch**ブロックを使用します。 それ以外の場合は、 **GetErrorInfo** を呼び出すことによって、明示的にエラー オブジェクトを取得する必要があります。 次の Visual Basic の sub プロシージャでは、ADO エラーをトラッピングする方法を示します。

```vb 
 
' BeginErrorHandlingVB01 
Private Sub Form_Load() 
 ' Turn on error handling 
 On Error GoTo FormLoadError 
 
 'Open the database and the recordset for processing. 
 ' 
 Dim strCnn As String 
 strCnn = "Provider='sqloledb';" & _ 
 "Data Source='MySqlServer';" & _ 
 "Initial Catalog='Northwind';Integrated Security='SSPI';" 
 
 ' cnn is a Public Connection Object because 
 ' it was defined WithEvents 
 Set cnn = New ADODB.Connection 
 cnn.Open strCnn 
 
 ' The next line of code intentionally causes 
 ' an error by trying to open a connection 
 ' that has already been opened. 
 cnn.Open strCnn 
 
 ' rst is a Public Recordset because it 
 ' was defined WithEvents 
 Set rst = New ADODB.Recordset 
 rst.Open "Customers", cnn 
 
 Exit Sub 
 
' Error handler 
FormLoadError: 
 Dim strErr As String 
 Select Case Err 
 Case adErrObjectOpen 
 strErr = "Error #" & Err.Number & ": " & Err.Description & vbCrLf 
 strErr = strErr & "Error reported by: " & Err.Source & vbCrLf 
 strErr = strErr & "Help File: " & Err.HelpFile & vbCrLf 
 strErr = strErr & "Topic ID: " & Err.HelpContext 
 MsgBox strErr 
 Debug.Print strErr 
 Err.Clear 
 Resume Next 
 ' If some other error occurs that 
 ' has nothing to do with ADO, show 
 ' the number and description and exit. 
 Case Else 
 strErr = "Error #" & Err.Number & ": " & Err.Description & vbCrLf 
 MsgBox strErr 
 Debug.Print strErr 
 Unload Me 
 End Select 
End Sub 
' EndErrorHandlingVB01 
```

これは、**フォーム\_ロード**イベント プロシージャが 2 回、同じ**接続**オブジェクトを開こうとしてエラーを意図的に作成します。 **Open** メソッドが 2 度目に呼び出されたときに、エラー ハンドラーが起動されます。 この場合、エラーの種類は **adErrObjectOpen** であるため、プログラムの実行が再開される前に、エラー ハンドラーによって次のメッセージが表示されます。

```vb 
Error #3705: Operation is not allowed when the object is open. 
Error reported by: ADODB.Connection 
Help File: E:\WINNT\HELP\ADO260.CHM Topic ID: 1003705 
```

このエラー メッセージには、Visual Basic の **Err** オブジェクトによって提供される各種の情報が含まれています。ただし、 **LastDLLError** 値は、ここでは該当しないため、表示されません。エラー番号は、どのエラーが発生したのかを示します。説明は、エラーを自分で処理しない場合に便利です。この説明をユーザーにそのまま表示できるためです。通常はアプリケーション用にカスタマイズされたメッセージを使用する方がよいのですが、すべてのエラーを予測することはできません。説明は、どのような問題が発生したのかを知るための一定の手掛かりとなります。サンプル コードでは、 **Connection** オブジェクトによってエラーが報告されています。ここでは、変数名ではなく、オブジェクトの型またはプログラム識別子が示されます。


> [!NOTE]
> <P>[!メモ] Visual Basic の <STRONG>Err</STRONG> オブジェクトには、最新のエラーに関する情報のみが格納されます。 <STRONG>Connection</STRONG> オブジェクトの ADO の <STRONG>Errors</STRONG> コレクションには、直近の ADO 操作によって発生したエラー 1 つにつき 1 つの <STRONG>Error</STRONG> オブジェクトが含まれています。複数のエラーを処理するときは、 <STRONG>Err</STRONG> オブジェクトの代わりに <STRONG>Errors</STRONG> コレクションを使用します。 <STRONG>Errors</STRONG> コレクションの詳細については、「 <A href="provider-errors.md">プロバイダー エラー</A>」を参照してください。ただし、有効な <STRONG>Connection</STRONG> オブジェクトがない場合は、 <STRONG>Err</STRONG> オブジェクトが ADO エラーに関する唯一の情報源です。</P>



ADO エラーを発生させる可能性が高い操作とはどのようなものでしょうか。よくある ADO エラーは、 **Connection** や **Recordset** などのオブジェクトを開いたときや、データを更新しようとしたとき、プロバイダーがサポートしていないメソッドまたはプロパティを呼び出したときに発生するものです。

OLE DB エラーも、 **Errors** コレクションで実行時エラーとしてアプリケーションに渡すことができます。OLE DB のエラー番号の詳細については、「OLE DB Programmer's ReferenceOLE DB Programmer's Reference」 (英語) の Chapter 16 を参照してください。

