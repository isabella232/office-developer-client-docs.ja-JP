---
title: オフライン ソリューションを操作する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- オフライン ソリューション [infopath 2007],ソリューション [InfoPath 2007], オフライン,InfoPath 2007,オフライン ソリューション
localization_priority: Normal
ms.assetid: 108f9bd0-c80f-4790-a572-da2f571a7d85
description: InfoPath オブジェクト モデルに用意されている Application クラスの MachineOnlineState プロパティを使用すると、ユーザーのコンピューターがネットワークに接続されているかどうかをフォーム コードで確認できます。MachineOnlineState プロパティの値を確認することにより、接続の状態に応じてフォーム コードで異なる処理を実行できます。
ms.openlocfilehash: eb2903c2445a61be803c0d7a2f5ddd7ac7a912ad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436140"
---
# <a name="work-with-offline-solutions"></a><span data-ttu-id="939b9-105">オフライン ソリューションを操作する</span><span class="sxs-lookup"><span data-stu-id="939b9-105">Work with offline solutions</span></span>

<span data-ttu-id="939b9-p102">InfoPath オブジェクト モデルに用意されている [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.MachineOnlineState.aspx) クラスの [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) プロパティを使用すると、ユーザーのコンピューターがネットワークに接続されているかどうかをフォーム コードで確認できます。 **MachineOnlineState** プロパティの値を確認することにより、接続の状態に応じてフォーム コードで異なる処理を実行できます。</span><span class="sxs-lookup"><span data-stu-id="939b9-p102">The InfoPath object model provides the [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.MachineOnlineState.aspx) property of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class that enables your form code to check whether the user's computer is connected to the network. By checking the value of **MachineOnlineState** property, your form code can perform different actions depending on the state of the connection.</span></span> 
  
## <a name="using-the-machineonlinestate-property"></a><span data-ttu-id="939b9-108">MachineOnlineState プロパティを使用する</span><span class="sxs-lookup"><span data-stu-id="939b9-108">Using the MachineOnlineState property</span></span>

<span data-ttu-id="939b9-109">次の例では、ユーザーのコンピューターがオンラインかオフラインかに基づいてフォームを送信する方法を決定するロジックを、フォーム コードに追加する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="939b9-109">The following example shows how you can add logic to your form code that determines how to submit a form based on whether the user's computer is online or offline.</span></span>
  
<span data-ttu-id="939b9-p103">この例では、販売報告書を送信するためのフォームが既に作成されているものとします。フォームには、報告書の対象期間 (年と月) を指定する period というフィールドがあります。また、データ接続、およびユーザーがオンラインのときに報告書を送信するロジックも既に定義されているものとします。</span><span class="sxs-lookup"><span data-stu-id="939b9-p103">This example assumes that you have created a form for submitting a sales report that contains a field named period that specifies the month and year covered in the report. It also assumes that you have already defined a data connection and the logic for submitting the report when the user is online.</span></span> 
  
### <a name="add-a-data-connection-that-submits-the-form-as-an-attachment-to-an-email-message"></a><span data-ttu-id="939b9-112">フォームを電子メール メッセージの添付ファイルとして送信するデータ接続を追加する</span><span class="sxs-lookup"><span data-stu-id="939b9-112">Add a data connection that submits the form as an attachment to an email message</span></span>

1. <span data-ttu-id="939b9-113">**空 (InfoPath エディター)** のテンプレートを使用して InfoPath フォーム テンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="939b9-113">Create an InfoPath form template using the **Blank (InfoPath Editor)** template.</span></span> 
    
2. <span data-ttu-id="939b9-114">InfoPath デザイン モードで、[ **データ**] タブの [ **データ接続**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="939b9-114">In InfoPath design mode, click **Data Connections** on the **Data** tab.</span></span> 
    
3. <span data-ttu-id="939b9-115">[ **データ接続**] ダイアログ ボックスで、[ **追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="939b9-115">In the **Data Connections** dialog box, click **Add**.</span></span>
    
4. <span data-ttu-id="939b9-116">**[データ接続ウィザード]** で、**[データの送信]** をクリックしてから、**[次へ]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="939b9-116">In the **Data Connection Wizard**, click **Submit data**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="939b9-117">ウィザードの次のページで、**[電子メール メッセージとして送信]** をクリックしてから、**[次へ]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="939b9-117">On the next page of the wizard, click **As an email message**, and then click **Next**.</span></span>
    
6. <span data-ttu-id="939b9-118">ウィザードの次のページで、**[宛先]** ボックスに自分の電子メール アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="939b9-118">On the next page of the wizard, type your email address in the **To** box.</span></span> 
    
7. <span data-ttu-id="939b9-119">**[件名]** ボックスで、次のようにして販売期間にテキスト「Sales Report」を組み合わせます。</span><span class="sxs-lookup"><span data-stu-id="939b9-119">In the **Subject** box, do the following to combine the sales period with the text Sales Report:</span></span> 
    
   1. <span data-ttu-id="939b9-120">[ **件名**] ボックスの横の [ **数式**] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="939b9-120">Click the **Formula** button next to the **Subject** box.</span></span> 
      
   2. <span data-ttu-id="939b9-121">[ **数式の挿入**] ダイアログ ボックスで、[ **関数の挿入**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="939b9-121">In the **Insert Formula** dialog box, click **Insert Function**.</span></span>
      
   3. <span data-ttu-id="939b9-122">[ **関数の挿入**] ダイアログ ボックスで、[ **カテゴリ**] ボックスの一覧の [ **文字列**] をクリックします。次に、[ **関数**] ボックスの一覧の [ **concat**] をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="939b9-122">In the **Insert Function** dialog box, click **Text** in the **Categories** list, and then double-click **concat** in the **Functions** list.</span></span> 
      
   4. <span data-ttu-id="939b9-123">[ **ダブルクリックしてフィールドを挿入してください**] の最初のインスタンスを、"Sales Report: " という文字列 (単一引用符を含む) に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="939b9-123">Replace the first instance of **double click to insert field** with the following (include the single quotes): 'Sales Report: '</span></span> 
      
   5. <span data-ttu-id="939b9-124">[ **ダブルクリックしてフィールドを挿入してください**] の 2 番目のインスタンスをダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="939b9-124">Double-click the second instance of **double click to insert field**.</span></span>
      
   6. <span data-ttu-id="939b9-125">[ **フィールドまたはグループの選択**] ダイアログ ボックスで、period フィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="939b9-125">In the **Select a Field or Group** dialog box, select the period field.</span></span> 
      
   7. <span data-ttu-id="939b9-126">[ **ダブルクリックしてフィールドを挿入してください**] の最後のインスタンスを削除し、[ **OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="939b9-126">Delete the final instance of **double click to insert field**, and then click **OK**.</span></span>
    
8. <span data-ttu-id="939b9-127">ウィザードで、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="939b9-127">In the wizard, click **Next**.</span></span>
    
9. <span data-ttu-id="939b9-128">ウィザードの次のページで、[ **添付ファイル名**] ボックスの横の [ **数式**] ボタンをクリックします。上記の手順を繰り返して concat("Sales Report - ", period) という式を作成し、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="939b9-128">On the next page of the wizard, click the **Formula** button next to the **Attachment Name** box, and then repeat the steps above to create the formula concat("Sales Report - ", period), and then click **Next**.</span></span>
    
10. <span data-ttu-id="939b9-129">ウィザードの最後のページで、**[このデータ接続の名前を入力してください]** ボックスに「E-mail Submit」と入力してから、**[完了]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="939b9-129">On the last page of the wizard, type Email Submit in the **Enter a name for this data connection** box, and then click **Finish**.</span></span>
    
### <a name="add-logic-for-submitting-the-form-depending-on-the-connected-state-of-a-users-computer"></a><span data-ttu-id="939b9-130">ユーザーのコンピューターの接続状態に応じてフォームを送信するためのロジックを追加する</span><span class="sxs-lookup"><span data-stu-id="939b9-130">Add logic for submitting the form depending on the connected state of a user's computer</span></span>

1. <span data-ttu-id="939b9-131">InfoPath デザイン モードで、[ **データ**] タブの [ **送信オプション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="939b9-131">In InfoPath design mode, click **Submit Options** on the **Data** tab.</span></span> 
    
2. <span data-ttu-id="939b9-132">[ **送信オプション**] ダイアログ ボックスで、[ **ユーザーによるこのフォームの送信を許可する**] をクリックします。次に、[ **コードを使用してユーザー設定操作を実行する**] を選択し、[ **コードの編集**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="939b9-132">In the **Submit Options** dialog box, click **Allow users to submit this form**, select **Perform custom action using Code**, click **Edit Code**.</span></span>
    
3. <span data-ttu-id="939b9-133">[Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) イベント ハンドラーの下に、次の 2 つの関数を追加します。</span><span class="sxs-lookup"><span data-stu-id="939b9-133">Add the following two functions below the [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) event handler:</span></span> 
    
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

4. <span data-ttu-id="939b9-134">**Submit** イベント ハンドラー関数に、次の [if](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) ステートメントを追加します。</span><span class="sxs-lookup"><span data-stu-id="939b9-134">Add the following **if** statement to the [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) event handler function.</span></span> 
    
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

### <a name="test-the-code"></a><span data-ttu-id="939b9-135">コードをテストする</span><span class="sxs-lookup"><span data-stu-id="939b9-135">Test the code</span></span>

1. <span data-ttu-id="939b9-136">[ **デバッグ**] メニューの [ **デバッグ開始**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="939b9-136">On the **Debug** menu, click **Start Debugging**.</span></span>
    
2. <span data-ttu-id="939b9-137">フォームにデータを入力します。</span><span class="sxs-lookup"><span data-stu-id="939b9-137">Fill out the form.</span></span>
    
3. <span data-ttu-id="939b9-138">Microsoft Internet Explorer を起動します。</span><span class="sxs-lookup"><span data-stu-id="939b9-138">Start Microsoft Internet Explorer.</span></span>
    
4. <span data-ttu-id="939b9-139">Internet Explorer で、[ **ファイル**] メニューの [ **オフライン作業**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="939b9-139">In Internet Explorer, click **Work offline** on the **File** menu.</span></span> 
    
5. <span data-ttu-id="939b9-140">InfoPath で、**[送信]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="939b9-140">In InfoPath, click **Submit**.</span></span> <span data-ttu-id="939b9-141">フォームが電子メール メッセージとして送信されることを示すメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="939b9-141">You should see a message that the form will be submitted as an email message.</span></span>
    
6. <span data-ttu-id="939b9-p105">[ **送信**] をクリックします。フォームがオフラインで送信されたこと、およびネットワーク接続時に送信されることを示すメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="939b9-p105">Click **Send**. You should see a message stating that the form has been submitted offline and will be submitted when you connect to the network.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="939b9-144">関連項目</span><span class="sxs-lookup"><span data-stu-id="939b9-144">See also</span></span>

- [<span data-ttu-id="939b9-145">オフラインで使用するフォーム テンプレートをデザインする</span><span class="sxs-lookup"><span data-stu-id="939b9-145">Design a form template for offline use</span></span>](https://support.office.com/en-us/article/design-a-form-template-for-offline-use-3ab8de84-babc-4bd7-9215-66d308546be4)

