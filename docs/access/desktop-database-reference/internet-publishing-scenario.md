---
title: Internet Publishing シナリオ
TOCTitle: Internet publishing scenario
ms:assetid: 25a3fa8b-86ec-9e72-5e62-bf0d849479b7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249024(v=office.15)
ms:contentKeyID: 48543790
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1f481c4bc5cf11f9345458b3859c099b40a79885
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026450"
---
# <a name="internet-publishing-scenario"></a>Internet Publishing シナリオ

**適用されます**Access 2013、Office 2013。

ここに示すコード例では、ADO を Microsoft OLE DB Provider for Internet Publishing と共に使用する方法を示します。このシナリオでは、 **Recordset** 、 **Record** 、および **Stream** の各オブジェクトを使用して Internet Publishing Provider で発行されたリソースのコンテンツを表示する Visual Basic アプリケーションを作成します。

このシナリオを作成するには、次の手順が必要です。 

1. Visual Basic プロジェクトを設定します。
2. メイン リスト ボックスを初期化します。
3. フィールドのリスト ボックスを作成します。
4. [詳細] テキスト ボックスを作成します。

## <a name="step-1-set-up-the-visual-basic-project"></a>手順 1: Visual Basic プロジェクトのセットアップします。

このシナリオでは、システムに Microsoft Visual Basic 6.0 以降、ADO 2.5 以降、および Microsoft OLE DB Provider for Internet Publishing がインストールされていることを前提としています。

### <a name="create-an-ado-project"></a>ADO プロジェクトを作成します。

1.  Microsoft Visual Basic で、新規の標準 EXE プロジェクトを作成します。

2.  **プロジェクト**] メニューの [**参照設定**] をクリックします。

3.  **Microsoft ActiveX データ オブジェクトの 2.5 ライブラリ**を選択し、し、[ **OK**] をクリックします。

### <a name="insert-controls-on-the-main-form"></a>メイン フォーム上のコントロールを挿入します。

1.  Form1 に ListBox コントロールを追加します。 **Name**プロパティを**lstMain**に設定します。

2.  Form1 にもう 1 つの ListBox コントロールを追加します。 **Name**プロパティを**lstDetails**に設定します。

3.  Form1 に TextBox コントロールを追加します。 **Name**プロパティを**txtDetails**に設定します。

## <a name="step-2-initialize-the-main-list-box"></a>手順 2: Main リスト ボックスを初期化します。

### <a name="declare-global-record-and-recordset-objects"></a>グローバル レコードとレコード セット オブジェクトを宣言します。

- Form1 の (General) (Declarations) に次のコードを挿入します。
    
   ```vb 
     
    Option Explicit 
    Dim grec As Record 
    Dim grs As Recordset 
   ```
    
   このコードによって、このシナリオで後ほど使用する **Record** オブジェクトと **Recordset** オブジェクトへのグローバル オブジェクト参照を宣言します。

### <a name="connect-to-a-url-and-populate-lstmain"></a>URL に接続し、lstMain に設定

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
    
   このコードによって、グローバルな **Record** オブジェクトと **Recordset** オブジェクトのインスタンスが作成されます。 **レコード** `grec` **ActiveConnection**として指定された URL を使用して開かれました。 URL が存在する場合は開かれますが、存在しない場合は作成されます。 
   
   交換する必要があることに注意`https://servername/foldername/`お客様の環境からの有効な URL を使用しています。 
   
   **レコード セット** `grs` **レコード**の子に対して開かれた`grec`。 LstMain には、URL に公開されたリソースのファイル名が、表示されます。

## <a name="step-3-populate-the-fields-list-box"></a>手順 3: フィールド リスト ボックスを表示します。

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

   このコードを宣言し、ローカルの**レコード**と**レコード セット**オブジェクトのインスタンスを作成する`rec`と`rs`それぞれ。

   LstMain 内で選択されたリソースに対応する行の現在の行を加え、 `grs`。 **詳細**のリスト ボックスをオフにし、および`rec`の現在の行で開かれた`grs`ソースとして。

   リソースの場合、コレクションを記録 (指定されている**RecordType**によって)、ローカル**レコード セット**`rs`の子で開かれた`rec`。 lstDetails の行から値を入力し、 `rs`。

   リソースが、単純なレコードの場合`recFields`と呼ばれます。 詳細については`recFields`、次の手順を参照してください。

   リソースが構造化ドキュメントである場合は、コードは実装されません。

## <a name="step-4-populate-the-details-text-box"></a>手順 4: [詳細] テキスト ボックスを作成します。

- という名前のサブルーチンを作成する`recFields`し、次のコードを挿入します。

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

   このコード フィールドが lstDetails に設定し、単純なレコードの値に渡される`recFields`。 リソースがテキスト ファイルである場合は、テキスト **Stream** がリソース レコードから開かれます。 コードかどうかを文字セットは ASCII に**ストリーム**の内容をコピー `txtDetails`。

