---
title: InfoPath オブジェクト モデルを使用してオフライン ソリューションを操作する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- ソリューション [infopath 2007], オフライン,オフライン ソリューション [InfoPath 2007], InfoPath 2003 互換のフォーム テンプレート,InfoPath 2003 互換のフォーム テンプレート, オフライン ソリューション
localization_priority: Normal
ms.assetid: 634ccd8c-0b5f-4161-875c-0e546a517377
description: InfoPath 2003 互換オブジェクト モデルに用意されている Application オブジェクトの MachineOnlineState プロパティを使用すると、ユーザーのコンピューターがネットワークに接続されているかどうかをフォーム コードで確認できます。
ms.openlocfilehash: 452eb0d92b09dc0c3f9b2c247f7cda243dc8eb13
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303571"
---
# <a name="work-with-offline-solutions-using-the-infopath-object-model"></a>InfoPath オブジェクト モデルを使用してオフライン ソリューションを操作する

InfoPath 2003 互換オブジェクト モデルに用意されている [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.MachineOnlineState.aspx) オブジェクトの [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) プロパティを使用すると、ユーザーのコンピューターがネットワークに接続されているかどうかをフォーム コードで確認できます。 
  
## <a name="using-the-machineonlinestate-property"></a>MachineOnlineState プロパティを使用する

次の例では、ユーザーのコンピューターがオンラインかオフラインかに基づいてフォームを送信する方法を決定するロジックを、フォーム コードに追加する方法を示します。
  
この例では、販売報告書を送信するためのフォームが既に作成されているものとします。フォームには、報告書の対象期間 (年と月) を指定する "period" というフィールドがあります。また、データ接続、およびユーザーがオンラインのときに報告書を送信するロジックも既に定義されているものとします。
  
### <a name="add-a-data-connection-that-submits-the-form-as-an-attachment-to-an-email-message"></a>フォームを電子メール メッセージの添付ファイルとして送信するデータ接続を追加する

1. InfoPath マネージ コード フォーム テンプレートを作成または開きます。
    
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
    
8. ウィザードで **[次へ]** をクリックします。
    
9. ウィザードの次のページで、**[このデータ接続の名前を入力してください]** ボックスに「E-mail Submit」と入力し、**[完了]** をクリックします。
    
### <a name="add-logic-for-submitting-the-form-depending-on-the-connected-state-of-a-users-computer"></a>ユーザーのコンピューターの接続状態に応じてフォームを送信するためのロジックを追加する

1. InfoPath デザイン モードで、[ **データ**] タブの [ **送信オプション**] をクリックします。
    
2. [ **送信オプション**] ダイアログ ボックスで [ **ユーザーによるこのフォームの送信を許可する**] をクリックし、[ **コードを使用してユーザー設定操作を実行する**] を選択します。
    
3. [ **コードの編集**] ボタンをクリックします。 
    
4. [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) イベント ハンドラーの下に、次の 2 つの関数を追加します。 
    
   ```cs
    public void OnlineSubmit(DocReturnEvent e)
    {
      // Logic for submitting online goes here.
    }
    public void OfflineSubmitX(DocReturnEvent e)
    {
      // Access and submit to the email adapter.
      DataAdaptersCollection myDataAdapters = 
          thisXDocument.DataAdapters;
      EmailAdapterObject submitAdapter = 
          (EmailAdapterObject) myDataAdapters["Email Submit"];
      submitAdapter.Submit();
      // Notify the user that the form was submitted offline.
      System.Text.StringBuilder message = 
      new System.Text.StringBuilder();
      message.Append("You submitted your Sales Report offline. ");
      message.Append("Your Sales Report is in your outbox ");
      message.Append("and will be submitted when you connect to ");
      message.Append("the network.");
        thisXDocument.UI.Alert(message.ToString());
      // The submission was successful.
      e.ReturnStatus = true;
    }
   ```

5. **OnSubmitRequest** イベント ハンドラー関数に、次の **if** ステートメントを追加します。 
    
   ```cs
    // Check the computer's connection state.
    if (thisApplication.MachineOnlineState==XdMachineOnlineState.xdOnline)
    {
        OnlineSubmit(e);
    }
    else
    {
        OfflineSubmit(e);
    }
   ```

### <a name="test-the-code"></a>コードをテストする

1. InfoPath デザイン モードで、[ **ホーム**] タブの [ **プレビュー**] をクリックします。 
    
2. フォームにデータを入力します。
    
3. Microsoft Internet Explorer を起動します。
    
4. Internet Explorer で、[ **ファイル**] メニューの [ **オフライン作業**] をクリックします。 
    
5. InfoPath で、**[送信]** をクリックします。 フォームが電子メール メッセージとして送信されることを示すメッセージが表示されます。
    
6. **[送信]** をクリックします。フォームがオフラインで送信されたことを示すメッセージが表示されます。
    

