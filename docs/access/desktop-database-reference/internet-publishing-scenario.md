---
title: Internet Publishing シナリオ
TOCTitle: Internet publishing scenario
ms:assetid: 25a3fa8b-86ec-9e72-5e62-bf0d849479b7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249024(v=office.15)
ms:contentKeyID: 48543790
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0f28b14f3eaf6792a74ef0967d698d5a3914955a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291273"
---
# <a name="internet-publishing-scenario"></a>Internet Publishing シナリオ

**適用先:** Access 2013、Office 2013

ここに示すコード例では、ADO を Microsoft OLE DB Provider for Internet Publishing と共に使用する方法を示します。このシナリオでは、 **Recordset** 、 **Record** 、および **Stream** の各オブジェクトを使用して Internet Publishing Provider で発行されたリソースのコンテンツを表示する Visual Basic アプリケーションを作成します。

このシナリオを作成するには、次の手順が必要です。 

1. Visual Basic プロジェクトをセットアップします。
2. メインリストボックスを初期化します。
3. [Fields] リストボックスに値を設定します。
4. [詳細] テキストボックスに値を設定します。

## <a name="step-1-set-up-the-visual-basic-project"></a>手順 1: Visual Basic プロジェクトをセットアップする

このシナリオでは、システムに Microsoft Visual Basic 6.0 以降、ADO 2.5 以降、および Microsoft OLE DB Provider for Internet Publishing がインストールされていることを前提としています。

### <a name="create-an-ado-project"></a>ADO プロジェクトを作成する

1.  Microsoft Visual Basic で、新規の標準 EXE プロジェクトを作成します。

2.  From the **Project** menu, choose **References**.

3.  [ **Microsoft ActiveX データオブジェクト2.5 ライブラリ**] を選択し、[ **OK**] をクリックします。

### <a name="insert-controls-on-the-main-form"></a>メインフォームにコントロールを挿入する

1.  Form1 に ListBox コントロールを追加します。 **Name**プロパティを**lstMain**に設定します。

2.  Form1 にもう 1 つの ListBox コントロールを追加します。 **Name**プロパティを**lstDetails**に設定します。

3.  Form1 に TextBox コントロールを追加します。 " **Name/名前**" プロパティを**txtdetails**に設定します。

## <a name="step-2-initialize-the-main-list-box"></a>手順 2: メインリストボックスを初期化する

### <a name="declare-global-record-and-recordset-objects"></a>グローバルレコードオブジェクトと Recordset オブジェクトを宣言する

- Form1 の (General) (Declarations) に次のコードを挿入します。
    
   ```vb 
     
    Option Explicit 
    Dim grec As Record 
    Dim grs As Recordset 
   ```
    
   このコードによって、このシナリオで後ほど使用する **Record** オブジェクトと **Recordset** オブジェクトへのグローバル オブジェクト参照を宣言します。

### <a name="connect-to-a-url-and-populate-lstmain"></a>URL に接続し、lstMain に入力します。

- Form1 の Form Load イベント ハンドラーに次のコードを挿入します。
    
   ```vb 
     
    Private Sub Form_Load() 
        Set grec = New Record 
        Set grs = New Recordset 
        grec.Open "", "URL=https://servername/foldername/", , _ 
            adOpenIfExists Or adCreateCollection 
        Set grs = grec.GetChildren 
        While Not grs.EOF 
            lstMain.AddItem grs(0) 
            grs.MoveNext 
        Wend 
    End Sub 
   ```
    
   このコードによって、グローバルな **Record** オブジェクトと **Recordset** オブジェクトのインスタンスが作成されます。 **ActiveConnection**として指定された URL を使用して、 **Record** `grec`が開かれます。 URL が存在する場合は開かれますが、存在しない場合は作成されます。 
   
   ご使用の環境から`https://servername/foldername/`有効な URL に置き換える必要があることに注意してください。 
   
   **Recordset** `grs`は、 **Record** `grec`の子に対して開かれます。 lstMain には、URL に発行されたリソースのファイル名が設定されます。

## <a name="step-3-populate-the-fields-list-box"></a>手順 3: Fields リストボックスに値を設定する

- lstMain の Click イベント ハンドラーに次のコードを挿入します。

   ```vb 
    
    Private Sub lstMain_Click() 
        Dim rec As Record 
        Dim rs As Recordset 
        Set rec = New Record 
        Set rs = New Recordset 
        grs.MoveFirst 
        grs.Move lstMain.ListIndex 
        lstDetails.Clear 
        rec.Open grs 
        Select Case rec.RecordType 
            Case adCollectionRecord: 
                Set rs = rec.GetChildren 
                While Not rs.EOF 
                    lstDetails.AddItem rs(0) 
                    rs.MoveNext 
                Wend 
            Case adSimpleRecord: 
                recFields rec, lstDetails, txtDetails 
                
            Case adStructDoc: 
        End Select 
        
    End Sub 
   ```

   このコードでは、ローカルの**Record**オブジェクトと`rec` **Recordset**オブジェクトの宣言とインスタンス化を`rs`それぞれ行います。

   lstMain で選択されているリソースに対応する行が、の`grs`現在の行になります。 その後、**詳細**リストボックスがクリア`rec`され、ソースとして`grs`の現在の行を使用して開きます。

   リソースが**RecordType**で指定されているようにコレクションレコードである場合、ローカルの**Recordset** `rs`はの`rec`子で開かれます。 lstDetails には、の`rs`行の値が入力されます。

   リソースが単純なレコードである場合`recFields`は、が呼び出されます。 の詳細につい`recFields`ては、次の手順を参照してください。

   リソースが構造化ドキュメントである場合は、コードは実装されません。

## <a name="step-4-populate-the-details-text-box"></a>手順 4: [詳細] テキストボックスに値を設定する

- という名前`recFields`の新しいサブルーチンを作成し、次のコードを挿入します。

   ```vb 
    
    Sub recFields(r As Record, l As ListBox, t As TextBox) 
        Dim f As Field 
        Dim s As Stream 
        Set s = New Stream 
        Dim str As String 
        
        For Each f In r.Fields 
            l.AddItem f.Name & ": " & f.Value 
        Next 
        t.Text = "" 
        If r!RESOURCE_CONTENTCLASS = "text/plain" Then 
            s.Open r, adModeRead, adOpenStreamFromRecord 
            str = s.ReadText(1) 
            s.Position = 0 
            If Asc(Mid(str, 1, 1)) = 63 Then '//63 = "?" 
                s.Charset = "ascii" 
                s.Type = adTypeText 
            End If 
            t.Text = s.ReadText(adReadAll) 
        End If 
    End Sub 
   ```

   このコードによって、lstDetails に`recFields`、渡される単純なレコードのフィールドと値が設定されます。 リソースがテキスト ファイルである場合は、テキスト **Stream** がリソース レコードから開かれます。 コードは、文字セットが ASCII であるかどうかを**** 判断し、 `txtDetails`ストリームの内容をにコピーします。

