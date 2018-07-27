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
ms.openlocfilehash: 858b5d317cf5245dbfb447fa9e118a11ecbe7eb3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799120"
---
# <a name="work-with-offline-solutions-using-the-infopath-object-model"></a><span data-ttu-id="653d3-105">InfoPath オブジェクト モデルを使用してオフライン ソリューションを操作する</span><span class="sxs-lookup"><span data-stu-id="653d3-105">Work with offline solutions using the InfoPath object model</span></span>

<span data-ttu-id="653d3-p102">InfoPath 2003 互換オブジェクト モデルに用意されている [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.MachineOnlineState.aspx) オブジェクトの [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) プロパティを使用すると、ユーザーのコンピューターがネットワークに接続されているかどうかをフォーム コードで確認できます。</span><span class="sxs-lookup"><span data-stu-id="653d3-p102">The InfoPath 2003-compatible object model provides the [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.MachineOnlineState.aspx) property of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) object which enables your form code to check whether the user's computer is connected to the network. Your form code can perform different actions depending on the state of the connection.</span></span> 
  
## <a name="using-the-machineonlinestate-property"></a><span data-ttu-id="653d3-108">MachineOnlineState プロパティを使用する</span><span class="sxs-lookup"><span data-stu-id="653d3-108">Using the MachineOnlineState Property</span></span>

<span data-ttu-id="653d3-109">次の例では、ユーザーのコンピューターがオンラインかオフラインかに基づいてフォームを送信する方法を決定するロジックを、フォーム コードに追加する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="653d3-109">The following example shows how you can add logic to your form code that determines how to submit a form based on whether the user's computer is online or offline.</span></span>
  
<span data-ttu-id="653d3-p103">この例では、販売報告書を送信するためのフォームが既に作成されているものとします。フォームには、報告書の対象期間 (年と月) を指定する "period" というフィールドがあります。また、データ接続、およびユーザーがオンラインのときに報告書を送信するロジックも既に定義されているものとします。</span><span class="sxs-lookup"><span data-stu-id="653d3-p103">This example assumes that you have created a form for submitting a sales report that contains a field named "period" that specifies the month and year covered in the report. It also assumes that you have already defined a data connection and the logic for submitting the report when the user is online.</span></span>
  
### <a name="add-a-data-connection-that-submits-the-form-as-an-attachment-to-an-email-message"></a><span data-ttu-id="653d3-112">フォームを電子メール メッセージの添付ファイルとして送信するデータ接続を追加する</span><span class="sxs-lookup"><span data-stu-id="653d3-112">Add a data connection that submits the form as an attachment to an e-mail message</span></span>

1. <span data-ttu-id="653d3-113">InfoPath マネージ コード フォーム テンプレートを作成または開きます。</span><span class="sxs-lookup"><span data-stu-id="653d3-113">Create or open an InfoPath managed-code form template.</span></span>
    
2. <span data-ttu-id="653d3-114">InfoPath デザイン モードで、[ **データ**] タブの [ **データ接続**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="653d3-114">In InfoPath design mode, on the **Data** tab, click **Data Connections**.</span></span>
    
3. <span data-ttu-id="653d3-115">[ **データ接続**] ダイアログ ボックスで、[ **追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="653d3-115">In the **Data Connections** dialog box, click **Add**.</span></span>
    
4. <span data-ttu-id="653d3-116">**[データ接続ウィザード]** で、**[データの送信]** をクリックしてから、**[次へ]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="653d3-116">In the **Data Connection Wizard**, click **Submit data**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="653d3-117">ウィザードの次のページで、**[電子メール メッセージとして送信]** をクリックしてから、**[次へ]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="653d3-117">On the next page of the wizard, click **As an e-mail message**, and then click **Next**.</span></span>
    
6. <span data-ttu-id="653d3-118">ウィザードの次のページで、**[宛先]** ボックスに自分の電子メール アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="653d3-118">On the next page of the wizard, type your e-mail address in the **To** box.</span></span> 
    
7. <span data-ttu-id="653d3-119">**[件名]** ボックスで、次のようにして販売期間にテキスト「Sales Report」を組み合わせます。</span><span class="sxs-lookup"><span data-stu-id="653d3-119">In the **Subject** box, do the following to combine the sales period with the text Sales Report:</span></span> 
    
   1. <span data-ttu-id="653d3-120">[ **件名**] ボックスの横の [ **数式**] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="653d3-120">Click the **Formula** button next to the **Subject** box.</span></span> 
      
   2. <span data-ttu-id="653d3-121">[ **数式の挿入**] ダイアログ ボックスで、[ **関数の挿入**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="653d3-121">In the **Insert Formula** dialog box, click **Insert Function**.</span></span>
      
   3. <span data-ttu-id="653d3-122">[ **関数の挿入**] ダイアログ ボックスで、[ **カテゴリ**] ボックスの一覧の [ **文字列**] をクリックします。次に、[ **関数**] ボックスの一覧の [ **concat**] をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="653d3-122">In the **Insert Function** dialog box, click **Text** in the **Categories** list, and then double-click **concat** in the **Functions** list.</span></span> 
      
   4. <span data-ttu-id="653d3-123">[ **ダブルクリックしてフィールドを挿入してください**] の最初のインスタンスを、"Sales Report: " という文字列 (単一引用符を含む) に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="653d3-123">Replace the first instance of **double click to insert field** with the following (include the single quotes): 'Sales Report: '</span></span> 
      
   5. <span data-ttu-id="653d3-124">[ **ダブルクリックしてフィールドを挿入してください**] の 2 番目のインスタンスをダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="653d3-124">Double-click the second instance of **double click to insert field**.</span></span>
      
   6. <span data-ttu-id="653d3-125">[ **フィールドまたはグループの選択**] ダイアログ ボックスで、period フィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="653d3-125">In the **Select a Field or Group** dialog box, select the period field.</span></span> 
      
   7. <span data-ttu-id="653d3-126">[ **ダブルクリックしてフィールドを挿入してください**] の最後のインスタンスを削除し、[ **OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="653d3-126">Delete the final instance of **double click to insert field**, and then click **OK**.</span></span>
    
8. <span data-ttu-id="653d3-127">ウィザードで **[次へ]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="653d3-127">In the wizard, click **Next**.</span></span>
    
9. <span data-ttu-id="653d3-128">ウィザードの次のページで、**[このデータ接続の名前を入力してください]** ボックスに「E-mail Submit」と入力し、**[完了]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="653d3-128">On the next page of the wizard, type 'E-mail Submit' in the **Enter a name for this data connection** box, and then click **Finish**.</span></span>
    
### <a name="add-logic-for-submitting-the-form-depending-on-the-connected-state-of-a-users-computer"></a><span data-ttu-id="653d3-129">ユーザーのコンピューターの接続状態に応じてフォームを送信するためのロジックを追加する</span><span class="sxs-lookup"><span data-stu-id="653d3-129">Add logic for submitting the form depending on the connected state of a user's computer</span></span>

1. <span data-ttu-id="653d3-130">InfoPath デザイン モードで、[ **データ**] タブの [ **送信オプション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="653d3-130">In InfoPath design mode, on the **Data** tab, click **Submit Options**.</span></span>
    
2. <span data-ttu-id="653d3-131">[ **送信オプション**] ダイアログ ボックスで [ **ユーザーによるこのフォームの送信を許可する**] をクリックし、[ **コードを使用してユーザー設定操作を実行する**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="653d3-131">In the **Submit Options** dialog box, click **Allow users to submit this form**, and then select **Perform custom action using Code**.</span></span>
    
3. <span data-ttu-id="653d3-132">[ **コードの編集**] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="653d3-132">Click the **Edit Code** button.</span></span> 
    
4. <span data-ttu-id="653d3-133">[OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) イベント ハンドラーの下に、次の 2 つの関数を追加します。</span><span class="sxs-lookup"><span data-stu-id="653d3-133">Add the following two functions below the [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) event handler:</span></span> 
    
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

5. <span data-ttu-id="653d3-134">**OnSubmitRequest** イベント ハンドラー関数に、次の **if** ステートメントを追加します。</span><span class="sxs-lookup"><span data-stu-id="653d3-134">Add the following **if** statement to the **OnSubmitRequest** event handler function.</span></span> 
    
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

### <a name="test-the-code"></a><span data-ttu-id="653d3-135">コードをテストする</span><span class="sxs-lookup"><span data-stu-id="653d3-135">Test the code</span></span>

1. <span data-ttu-id="653d3-136">InfoPath デザイン モードで、[ **ホーム**] タブの [ **プレビュー**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="653d3-136">In the InfoPath designer, click **Preview** on the **Home** tab.</span></span> 
    
2. <span data-ttu-id="653d3-137">フォームにデータを入力します。</span><span class="sxs-lookup"><span data-stu-id="653d3-137">Fill out the form.</span></span>
    
3. <span data-ttu-id="653d3-138">Microsoft Internet Explorer を起動します。</span><span class="sxs-lookup"><span data-stu-id="653d3-138">Start Microsoft Internet Explorer.</span></span>
    
4. <span data-ttu-id="653d3-139">Internet Explorer で、[ **ファイル**] メニューの [ **オフライン作業**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="653d3-139">In Internet Explorer, click **Work offline** on the **File** menu.</span></span> 
    
5. <span data-ttu-id="653d3-140">InfoPath で **[送信]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="653d3-140">In InfoPath, click **Submit**.</span></span> <span data-ttu-id="653d3-141">フォームが電子メール メッセージとして送信されることを示すメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="653d3-141">You should see a message that the form will be submitted as an e-mail message.</span></span>
    
6. <span data-ttu-id="653d3-p105">**[送信]** をクリックします。フォームがオフラインで送信されたことを示すメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="653d3-p105">Click **Send**. You should see a message stating that the form has been submitted offline.</span></span>
    

