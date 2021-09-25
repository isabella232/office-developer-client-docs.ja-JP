---
title: オフライン ソリューションを操作する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- オフライン ソリューション [infopath 2007],ソリューション [InfoPath 2007], オフライン,InfoPath 2007,オフライン ソリューション
ms.localizationpriority: medium
ms.assetid: 108f9bd0-c80f-4790-a572-da2f571a7d85
description: InfoPath オブジェクト モデルに用意されている Application クラスの MachineOnlineState プロパティを使用すると、ユーザーのコンピューターがネットワークに接続されているかどうかをフォーム コードで確認できます。MachineOnlineState プロパティの値を確認することにより、接続の状態に応じてフォーム コードで異なる処理を実行できます。
ms.openlocfilehash: 3bba72619e5f09a69e2b9b2666dfba77c0ed1dab
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605541"
---
# <a name="work-with-offline-solutions"></a>オフライン ソリューションを操作する

InfoPath オブジェクト モデルに用意されている [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.MachineOnlineState.aspx) クラスの [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) プロパティを使用すると、ユーザーのコンピューターがネットワークに接続されているかどうかをフォーム コードで確認できます。 **MachineOnlineState** プロパティの値を確認することにより、接続の状態に応じてフォーム コードで異なる処理を実行できます。 
  
## <a name="using-the-machineonlinestate-property"></a>MachineOnlineState プロパティを使用する

次の例では、ユーザーのコンピューターがオンラインかオフラインかに基づいてフォームを送信する方法を決定するロジックを、フォーム コードに追加する方法を示します。
  
この例では、販売報告書を送信するためのフォームが既に作成されているものとします。フォームには、報告書の対象期間 (年と月) を指定する period というフィールドがあります。また、データ接続、およびユーザーがオンラインのときに報告書を送信するロジックも既に定義されているものとします。 
  
### <a name="add-a-data-connection-that-submits-the-form-as-an-attachment-to-an-email-message"></a>フォームを電子メール メッセージの添付ファイルとして送信するデータ接続を追加する

1. **空 (InfoPath エディター)** のテンプレートを使用して InfoPath フォーム テンプレートを作成します。 
    
2. InfoPath デザイン モードで、[ **データ**] タブの [ **データ接続**] をクリックします。 
    
3. [ **データ接続**] ダイアログ ボックスで、[ **追加**] をクリックします。
    
4. **[データ接続ウィザード]** で、**[データの送信]** をクリックしてから、**[次へ]** をクリックします。
    
5. ウィザードの次のページで、**[電子メール メッセージとして送信]** をクリックしてから、**[次へ]** をクリックします。
    
6. ウィザードの次のページで、**[宛先]** ボックスに自分の電子メール アドレスを入力します。 
    
7. **[件名]** ボックスで、次のようにして販売期間にテキスト「Sales Report」を組み合わせます。 
    
   1. [ **件名**] ボックスの横の [ **数式**] ボタンをクリックします。 
      
   2. [ **数式の挿入**] ダイアログ ボックスで、[ **関数の挿入**] をクリックします。
      
   3. [ **関数の挿入**] ダイアログ ボックスで、[ **カテゴリ**] ボックスの一覧の [ **文字列**] をクリックします。次に、[ **関数**] ボックスの一覧の [ **concat**] をダブルクリックします。 
      
   4. [ **ダブルクリックしてフィールドを挿入してください**] の最初のインスタンスを、"Sales Report: " という文字列 (単一引用符を含む) に置き換えます。 
      
   5. [ **ダブルクリックしてフィールドを挿入してください**] の 2 番目のインスタンスをダブルクリックします。
      
   6. [ **フィールドまたはグループの選択**] ダイアログ ボックスで、period フィールドを選択します。 
      
   7. [ **ダブルクリックしてフィールドを挿入してください**] の最後のインスタンスを削除し、[ **OK**] をクリックします。
    
8. ウィザードで、[ **次へ**] をクリックします。
    
9. ウィザードの次のページで、[ **添付ファイル名**] ボックスの横の [ **数式**] ボタンをクリックします。上記の手順を繰り返して concat("Sales Report - ", period) という式を作成し、[ **次へ**] をクリックします。
    
10. ウィザードの最後のページで、**[このデータ接続の名前を入力してください]** ボックスに「E-mail Submit」と入力してから、**[完了]** をクリックします。
    
### <a name="add-logic-for-submitting-the-form-depending-on-the-connected-state-of-a-users-computer"></a>ユーザーのコンピューターの接続状態に応じてフォームを送信するためのロジックを追加する

1. InfoPath デザイン モードで、[ **データ**] タブの [ **送信オプション**] をクリックします。 
    
2. [ **送信オプション**] ダイアログ ボックスで、[ **ユーザーによるこのフォームの送信を許可する**] をクリックします。次に、[ **コードを使用してユーザー設定操作を実行する**] を選択し、[ **コードの編集**] をクリックします。
    
3. [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) イベント ハンドラーの下に、次の 2 つの関数を追加します。 
    
   ```cs
    public void OnlineSubmit(SubmitEventArgs e)
    {
      // Logic for submitting online goes here.
    }
    public void OfflineSubmit(SubmitEventArgs e)
    {
      // Access and submit to the email connection.
      DataConnectionCollection myDataConnections =
          this.DataConnections;
      EmailSubmitConnection submitConnection =
          (EmailSubmitConnection)myDataConnections["Email Submit"];
      submitConnection.Execute();
      // Notify the user that the form was submitted offline.
      System.Text.StringBuilder myMessage = 
          new System.Text.StringBuilder();
      myMessage.Append("You submitted your Sales Report offline. ");
      myMessage.Append("Your Sales Report is in your outbox ");
      myMessage.Append("and will be submitted when you connect to ");
      myMessage.Append("the network.");
        MessageBox.Show(myMessage.ToString());
      // The submission was successful.
      e.CancelableArgs.Cancel = false;
    }
   ```

   ```vb
    Public Sub OnlineSubmit(ByVal e As SubmitEventArgs)
      ' Logic for submitting online goes here.
    End Sub
    Public Sub OfflineSubmit(ByVal e As SubmitEventArgs)
      ' Access and submit to the email connection.
      Dim myDataConnections As DataConnectionCollection = _
          Me.DataConnections
      Dim submitConnection As EmailSubmitConnection = _
          DirectCast(myDataConnections("Email Submit"), _
          EmailSubmitConnection)
      submitConnection.Execute
      ' Notify the user that the form was submitted offline.
      Dim myMessage As System.Text.StringBuilder = _
          New System.Text.StringBuilder()
      myMessage.Append("You submitted your Sales Report offline. ")
      myMessage.Append("Your Sales Report is in your outbox ")
      myMessage.Append("and will be submitted when you connect to ")
      myMessage.Append("the network.")
        MessageBox.Show(myMessage.ToString())
      ' The submission was successful.
      e.CancelableArgs.Cancel = False
    End Sub
   ```

4. **Submit** イベント ハンドラー関数に、次の [if](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) ステートメントを追加します。 
    
   ```cs
    // Check the computer's connection state.
    if (this.Application.MachineOnlineState == MachineState.Online)
    {
      OnlineSubmit(e);
    }
    else
    {
      OfflineSubmit(e);
    }
   ```

   ```vb
    ' Check the computer's connection state.
    If (Me.Application.MachineOnlineState = MachineState.Online) Then
      OnlineSubmit(e)
    Else
    {
      OfflineSubmit(e)
    End If
   ```

### <a name="test-the-code"></a>コードをテストする

1. [ **デバッグ**] メニューの [ **デバッグ開始**] をクリックします。
    
2. フォームにデータを入力します。
    
3. Microsoft Internet Explorer を起動します。
    
4. Internet Explorer で、[ **ファイル**] メニューの [ **オフライン作業**] をクリックします。 
    
5. InfoPath で、**[送信]** をクリックします。 フォームが電子メール メッセージとして送信されることを示すメッセージが表示されます。
    
6. [ **送信**] をクリックします。フォームがオフラインで送信されたこと、およびネットワーク接続時に送信されることを示すメッセージが表示されます。
    
## <a name="see-also"></a>関連項目

- [オフラインで使用するフォーム テンプレートをデザインする](https://support.office.com/en-us/article/design-a-form-template-for-offline-use-3ab8de84-babc-4bd7-9215-66d308546be4)

