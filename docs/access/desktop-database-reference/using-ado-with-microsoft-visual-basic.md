---
title: Microsoft Visual Basic で ADO を使用する
TOCTitle: Using ADO with Microsoft Visual Basic
ms:assetid: 5e0fb2ec-42aa-e181-386f-099607ac7400
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249338(v=office.15)
ms:contentKeyID: 48545130
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 26eaa93a1abbb3778a2735d50dd5022edb3023d9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705240"
---
# <a name="using-ado-with-microsoft-visual-basic"></a>Microsoft Visual Basic での ADO の使用

**適用されます**Access 2013、Office 2013。

ADO プロジェクトのセットアップおよび ADO コードの作成は、Visual Basic と Visual Basic for Applications のどちらを使用する場合でもほとんど同じです。このトピックでは、Visual Basic と Visual Basic for Applications での ADO の使用方法と両者の相違点について説明します。

## <a name="referencing-the-ado-library"></a>ADO ライブラリを参照します。

プロジェクトでは ADO ライブラリを参照する必要があります。

### <a name="to-reference-ado-from-microsoft-visual-basic"></a>Microsoft Visual Basic から ADO を参照するには

1. Visual Basic で、[ **プロジェクト** ] メニューの [ **参照設定** ] をクリックします。

2. 一覧の [ **Microsoft ActiveX Data Objects x.x Library** ] をクリックします。少なくとも、次のライブラリが選択されていることを確認します。
   
   - Visual Basic for Applications
   - Visual Basic ランタイム オブジェクトとプロシージャ
   - Visual Basic オブジェクトとプロシージャ
   - OLE オートメーション

3. [ **OK** ] をクリックします。

たとえば、Microsoft Access を使用して、Visual Basic for Applications と同じように簡単に ADO を使用できます。

### <a name="to-reference-ado-from-microsoft-access"></a>Microsoft Access から ADO を参照するには

1. Microsoft Access の [ **データベース** ] ウィンドウの [ **モジュール** ] タブで、モジュールを選択または作成します。

2. [ **ツール** ] メニューの [ **参照設定** ] を選択します。

3. 一覧の [ **Microsoft ActiveX Data Objects x.x Library** ] をクリックします。少なくとも、次のライブラリが選択されていることを確認します。
    
   - Visual Basic for Applications
   - Microsoft Access 11.0 オブジェクト ライブラリ (またはそれ以降のバージョン)

4. [ **OK** ] をクリックします。

## <a name="creating-ado-objects-in-visual-basic"></a>Visual Basic で ADO オブジェクトを作成します。

オートメーション変数を作成し、その変数に対するオブジェクトのインスタンスを作成するには、 **Dim** メソッドまたは **CreateObject** メソッドを使用できます。

### <a name="dim"></a>Dim

**Dim** の **New** キーワードを使用すると、一度に ADO オブジェクトの作成とインスタンス化を行うことができます。

```vb 
 
Dim conn As New ADODB.Connection 
```

または、 **Dim** ステートメントの宣言とオブジェクトのインスタンス化を 2 段階で行うこともできます。

```vb 
 
Dim conn As ADODB.Connection 
Set conn = New ADODB.Connection 
```

> [!NOTE]
> プロジェクトで ADO ライブラリが正しく参照されていれば、**Dim** ステートメントで ADODB progid を明示的に使用する必要はありません。ただし、明示的に使用することで、他のライブラリとの命名の競合を確実に回避できます。
> 
> たとえば、同じプロジェクトに ADO と DAO に対する参照がどちらも含まれる場合は、 **Recordset** オブジェクトをインスタンス化するときに、次のコードで示すように、どちらのオブジェクト モデルを使用するのかを指定する修飾子を追加する必要があります。  
> 
> `Dim adoRS As ADODB.Recordset`  
>   
> `Dim daoRS As DAO.Recordset`

### <a name="createobject"></a>CreateObject

**CreateObject** メソッドでは、2 つの異なる手順で宣言とオブジェクトのインスタンス化を行う必要があります。

```vb 
 
Dim conn1 
Set conn1 = CreateObject("ADODB.Connection") As Object 
```

**CreateObject** でインスタンス化されたオブジェクトは、実行時にバインドされます。つまり、型が明確に決定されていないため、完全にコマンド ラインを確定できません。ただし、プロジェクトから ADO ライブラリに対する参照を省略することはでき、特定のバージョンのオブジェクトをインスタンス化できます。次に例を示します。

```vb 
 
Set conn1 = CreateObject("ADODB.Connection.2.0") As Object 
```

また、ADO Version 2.0 タイプ ライブラリに対する参照を明確に作成し、オブジェクトを作成することで、これを実現することもできます。

**CreateObject** メソッドでのオブジェクトのインスタンス化は、通常、 **Dim** ステートメントを使用する場合より時間がかかります。

## <a name="handling-events"></a>イベントを処理する

Microsoft Visual Basic での ADO イベントを処理するには、 **WithEvents**キーワードを使ってモジュール レベル変数を宣言する必要があります。 変数は、クラス モジュールの一部としてのみ宣言することができ、モジュール レベルで宣言する必要があります。 ADO イベントの処理の詳細についてを参照してください[第 7 章: ADO の処理イベントを](chapter-7-handling-ado-events.md)。

## <a name="visual-basic-examples"></a>Visual Basic の例

ADO のマニュアルには、Visual Basic での例が数多く含まれています。 詳細については、 [Microsoft Visual Basic で ADO コードの例](ado-code-examples-in-microsoft-visual-basic.md)を参照してください。

