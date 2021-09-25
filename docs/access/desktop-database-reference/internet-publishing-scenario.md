---
title: Internet Publishing シナリオ
TOCTitle: Internet publishing scenario
ms:assetid: 25a3fa8b-86ec-9e72-5e62-bf0d849479b7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249024(v=office.15)
ms:contentKeyID: 48543790
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 9a2216d41bd9d55e8b56816301350906fc2654a4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594112"
---
# <a name="internet-publishing-scenario"></a>Internet Publishing シナリオ

**適用先**: Access 2013、Office 2013

ここに示すコード例では、ADO を Microsoft OLE DB Provider for Internet Publishing と共に使用する方法を示します。このシナリオでは、 **Recordset** 、 **Record** 、および **Stream** の各オブジェクトを使用して Internet Publishing Provider で発行されたリソースのコンテンツを表示する Visual Basic アプリケーションを作成します。

このシナリオを作成するには、次の手順が必要です。 

1. プロジェクトのVisual Basicします。
2. [メイン] リスト ボックスを初期化します。
3. [フィールド] リスト ボックスに値を設定します。
4. [詳細] テキスト ボックスに値を設定します。

## <a name="step-1-set-up-the-visual-basic-project"></a>手順 1: プロジェクトのVisual Basicする

このシナリオでは、システムに Microsoft Visual Basic 6.0 以降、ADO 2.5 以降、および Microsoft OLE DB Provider for Internet Publishing がインストールされていることを前提としています。

### <a name="create-an-ado-project"></a>ADO プロジェクトを作成する

1.  Microsoft Visual Basic で、新規の標準 EXE プロジェクトを作成します。

2.  From the **Project** menu, choose **References**.

3.  [Microsoft **ActiveX データ オブジェクト 2.5 ライブラリ**] を選択し **、[OK] をクリックします**。

### <a name="insert-controls-on-the-main-form"></a>メイン フォームにコントロールを挿入する

1.  Form1 に ListBox コントロールを追加します。 Name プロパティ **を** **lstMain に設定します**。

2.  Form1 にもう 1 つの ListBox コントロールを追加します。 Name プロパティ **を** **lstDetails に設定します**。

3.  Form1 に TextBox コントロールを追加します。 Name プロパティ **を** **txtDetails に設定します**。

## <a name="step-2-initialize-the-main-list-box"></a>手順 2: [メイン] リスト ボックスを初期化する

### <a name="declare-global-record-and-recordset-objects"></a>グローバル Record オブジェクトと Recordset オブジェクトを宣言する

- Form1 の (General) (Declarations) に次のコードを挿入します。
    
   ```vb 
     
    Option Explicit 
    Dim grec As Record 
    Dim grs As Recordset 
   ```
    
   このコードによって、このシナリオで後ほど使用する **Record** オブジェクトと **Recordset** オブジェクトへのグローバル オブジェクト参照を宣言します。

### <a name="connect-to-a-url-and-populate-lstmain"></a>Connectにアクセスし、lstMain を設定する

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
    
   このコードによって、グローバルな **Record** オブジェクトと **Recordset** オブジェクトのインスタンスが作成されます。 レコード **は** `grec` **ActiveConnection** として指定された URL で開きます。 URL が存在する場合は開かれますが、存在しない場合は作成されます。 
   
   環境の有効な `https://servername/foldername/` URL に置き換える必要があります。 
   
   Recordset **は** `grs` Record の子で開 **きます** `grec` 。 その後、lstMain には、URL に発行されたリソースのファイル名が入力されます。

## <a name="step-3-populate-the-fields-list-box"></a>手順 3: [フィールド] リスト ボックスに値を設定する

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

   このコードは、ローカルの **Record** オブジェクトと **Recordset** オブジェクトをそれぞれ宣言し `rec` 、 `rs` インスタンス化します。

   lstMain で選択されたリソースに対応する行は、 の現在の行にされます `grs` 。 [ **詳細]** リスト ボックスがオフにされ、現在の行がソース `rec` `grs` として開きます。

   リソースがコレクション レコード **(RecordType** で指定) の場合、ローカル **Recordset** はの子で `rs` 開きます `rec` 。 次に、lstDetails の行の値が入力されます `rs` 。

   リソースが単純なレコードの場合は `recFields` 、呼び出されます。 詳細については、 `recFields` 次の手順を参照してください。

   リソースが構造化ドキュメントである場合は、コードは実装されません。

## <a name="step-4-populate-the-details-text-box"></a>手順 4: [詳細] テキスト ボックスに入力する

- という名前の新しいサブルーチンを作成 `recFields` し、次のコードを挿入します。

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

   このコードは、lstDetails に渡される単純なレコードのフィールドと値を設定します `recFields` 。 リソースがテキスト ファイルである場合は、テキスト **Stream** がリソース レコードから開かれます。 このコードは、文字セットが ASCII かどうかを決定し、Stream の内容 **をに** コピーします `txtDetails` 。

