---
title: イベント ハンドラーを追加する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- versionupgrade event [infopath 2007],handling events [InfoPath 2007],Changing event [InfoPath 2007],InfoPath 2007, adding event handlers,Changed event [InfoPath 2007],ContextChanged event [InfoPath 2007],Click event [InfoPath 2007],events [InfoPath 2007], adding event handlers,Sign event [InfoPath 2007],ViewSwitched event [InfoPath 2007],event handling [InfoPath 2007],Merge event [InfoPath 2007],Validating event [InfoPath 2007],Submit event [InfoPath 2007],Save event [InfoPath 2007],Loading event [InfoPath 2007]
localization_priority: Normal
ms.assetid: d69393fb-fb5a-4edb-abc0-38f5d7e80bcc
description: このトピックでは、Visual Studio 2012 を使用して Microsoft InfoPath マネージ コード フォーム テンプレートにイベント ハンドラーを追加する手順を説明します。イベント ハンドラーをフォーム テンプレートに追加するには、まず、InfoPath Designer でフォーム テンプレートを開き、コードを記述するイベントに対して適切なユーザー インターフェイス コマンドを選択します。 InfoPath Designer でイベントのコマンドを選択したら、Visual Studio 2012 コード エディターのそのイベントのスケルトン イベント ハンドラーに自動的にフォーカスが切り替わります。
ms.openlocfilehash: c6406ec1604355c59f4ee4818fdaea5d70f696bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300120"
---
# <a name="add-an-event-handler"></a><span data-ttu-id="b3bad-106">イベント ハンドラーを追加する</span><span class="sxs-lookup"><span data-stu-id="b3bad-106">Add an Event Handler</span></span>

<span data-ttu-id="b3bad-p102">このトピックでは、Visual Studio 2012 を使用して Microsoft InfoPath マネージ コード フォーム テンプレートにイベント ハンドラーを追加する手順を説明します。イベント ハンドラーをフォーム テンプレートに追加するには、まず、InfoPath Designer でフォーム テンプレートを開き、コードを記述するイベントに対して適切なユーザー インターフェイス コマンドを選択します。 InfoPath Designer でイベントのコマンドを選択したら、Visual Studio 2012 コード エディターのそのイベントのスケルトン イベント ハンドラーに自動的にフォーカスが切り替わります。</span><span class="sxs-lookup"><span data-stu-id="b3bad-p102">This topic describes the procedures for adding event handlers to an Microsoft InfoPath managed code form template using Visual Studio 2012. To add an event handler to a form template, you start with the form template open in the InfoPath Designer, and then select the appropriate user interface command for the event you want to write code for. After you select the command for an event in the InfoPath Designer, the focus automatically switches to the skeleton event handler for that event in the Visual Studio 2012 code editor.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="b3bad-p103">イベント ハンドラーを追加するには、必ず、InfoPath Designer のユーザー インターフェイスを使用してください。このユーザー インターフェイスでイベント ハンドラーを追加すると、フォーム テンプレート プロジェクトの FormCode.cs または FormCode.vb ファイルの **InternalStartup** メソッドにイベント バインド コードが生成されます。 **InternalStartup** メソッドを作成したり、このメソッドに自分でコードを追加したりしないでください。</span><span class="sxs-lookup"><span data-stu-id="b3bad-p103">You should always use the InfoPath Designer user interface to add an event handler. Adding an event handler with the user interface generates event binding code in the **InternalStartup** method of the FormCode.cs or FormCode.vb file in your form template project. You should not create the **InternalStartup** method or add any additional code within it yourself.</span></span> 
  
### <a name="add-an-event-handler-for-the-click-event-of-a-button-control"></a><span data-ttu-id="b3bad-113">ボタン コントロールの Click イベントに対するイベント ハンドラーを追加する</span><span class="sxs-lookup"><span data-stu-id="b3bad-113">Add an event handler for the Click event of a Button control</span></span>

1. <span data-ttu-id="b3bad-114">InfoPath Designer でフォーム テンプレートを開き、フォームに **ボタン** コントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="b3bad-114">Open the form template in the InfoPath Designer, and then add a **Button** control to the form.</span></span> 
    
2. <span data-ttu-id="b3bad-115">追加したボタンをクリックし、リボンの [ **プロパティ**] タブの [ **ユーザー設定コード**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b3bad-115">Click the button, and then on the **Properties** tab of the ribbon, click **Custom Code**.</span></span>
    
    <span data-ttu-id="b3bad-116">Visual Studio 2012 コード エディターの [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) イベントのスケルトン イベント ハンドラーにフォーカスが切り替わります。</span><span class="sxs-lookup"><span data-stu-id="b3bad-116">The focus switches to the skeleton event handler for the [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) event in the Visual Studio 2012 code editor.</span></span> 
    
### <a name="add-an-event-handler-for-the-changing-validating-or-changed-event-of-a-field-or-group"></a><span data-ttu-id="b3bad-117">フィールドまたはグループの Changing、Validating、または Changed イベントに対するイベント ハンドラーを追加する</span><span class="sxs-lookup"><span data-stu-id="b3bad-117">Add an event handler for the Changing, Validating, or Changed event of a field or group</span></span>

1. <span data-ttu-id="b3bad-118">InfoPath Designer でフォーム テンプレートを開きます。</span><span class="sxs-lookup"><span data-stu-id="b3bad-118">Open the form template in the InfoPath Designer.</span></span>
    
2. <span data-ttu-id="b3bad-119">たとえば [ **テキスト ボックス**] コントロールなど、フィールドまたはグループにバインドされたデータ入力コントロールを右クリックします。</span><span class="sxs-lookup"><span data-stu-id="b3bad-119">Right-click a data-entry control bound to the field or group, such as a **Text Box** control.</span></span> 
    
3. <span data-ttu-id="b3bad-p104">[ **プログラミング**] をポイントし、イベント ハンドラーを作成するイベントをクリックします。Visual Studio 2012 コード エディターの [Changing](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changing.aspx) 、 [Validating](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Validating.aspx) 、または [Changed](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changed.aspx) イベントのスケルトン イベント ハンドラーにフォーカスが切り替わります。</span><span class="sxs-lookup"><span data-stu-id="b3bad-p104">Point to **Programming**, and then click the event you want to create an event handler for. The focus switches to the skeleton event handler for the [Changing](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changing.aspx) , [Validating](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Validating.aspx) , or [Changed](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changed.aspx) event in the Visual Studio 2012 code editor.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="b3bad-p105">フォーム テンプレートの互換性設定が [ **Web ブラウザー フォーム**] に設定されている場合、 **Changing** イベントのイベント ハンドラーを作成するコマンドは使用できません。これは、InfoPath Forms Services を実行する Microsoft SharePoint Server 2010 上のドキュメント ライブラリに発行されたフォーム テンプレートのビジネス ロジックでは、 **Changing** イベントがサポートされていないためです。 **Changing** イベントのイベント ハンドラーを作成するには、InfoPath デザイン モードで互換性設定を [ **InfoPath エディター フォーム**] に変更する必要があります。これを行うには、[ **ファイル**] タブをクリックし、[ **フォームのオプション**]、[ **互換性**] の順にクリックして、[ **フォームの種類**] を [ **InfoPath エディター フォーム**] に設定します。</span><span class="sxs-lookup"><span data-stu-id="b3bad-p105">The command to create an event handler for the **Changing** event is not available if the compatibility setting for the form template is set to **Web Browser Form**. This is because the **Changing** event is not supported in the business logic of form templates published to document libraries on Microsoft SharePoint Server 2010 with InfoPath Forms Services. To create an event handler for the **Changing** event, you must change the compatibility setting to **InfoPath Editor** in the InfoPath designer. To do that, click the **File** tab, click **Form Options**, click **Compatibility**, and then set **Form type** to **InfoPath Editor Form**.</span></span> 
  
### <a name="add-an-event-handler-for-the-loading-viewswitched-contextchanged-and-sign-events-of-a-form"></a><span data-ttu-id="b3bad-126">フォームの Loading、ViewSwitched、ContextChanged、および Sign イベントに対するイベント ハンドラーを追加する</span><span class="sxs-lookup"><span data-stu-id="b3bad-126">Add an event handler for the Loading, ViewSwitched, ContextChanged, and Sign events of a form</span></span>

1. <span data-ttu-id="b3bad-127">InfoPath Designer でフォーム テンプレートを開きます。</span><span class="sxs-lookup"><span data-stu-id="b3bad-127">Open the form template in the InfoPath Designer.</span></span>
    
2. <span data-ttu-id="b3bad-128">リボンの [ **開発**] タブで、イベント ハンドラーを作成するフォーム イベントをクリックします。</span><span class="sxs-lookup"><span data-stu-id="b3bad-128">On the **Developer** tab of the ribbon, click the form event that you want to write an event handler for.</span></span> 
    
    <span data-ttu-id="b3bad-129">Visual Studio 2012 コード エディターの [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) 、 [ViewSwitched](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ViewSwitched.aspx) 、 [ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) 、または [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) イベントのスケルトン イベント ハンドラーにフォーカスが切り替わります。</span><span class="sxs-lookup"><span data-stu-id="b3bad-129">The focus switches to the skeleton event handler for the [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) , [ViewSwitched](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ViewSwitched.aspx) , [ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) , or [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) event in the Visual Studio 2012 code editor.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="b3bad-p106">フォーム テンプレートの互換性設定が [ [Web ブラウザー フォーム](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx)] に設定されている場合、[ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) または **Sign** イベントのイベント ハンドラーを作成するコマンドは使用できません。これは、InfoPath Forms Services を実行する Microsoft SharePoint Server 2010 上のドキュメント ライブラリに発行されたフォーム テンプレートのビジネス ロジックでは、それらのイベントがサポートされていないためです。 [ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) または [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) イベントのイベント ハンドラーを作成するには、InfoPath Designer で互換性設定を [ **InfoPath エディター フォーム**] に変更する必要があります。これを行うには、[ **ファイル**] タブをクリックし、[ **フォームのオプション**]、[ **互換性**] の順にクリックして、[ **フォームの種類**] を [ **InfoPath エディター フォーム**] に設定します。</span><span class="sxs-lookup"><span data-stu-id="b3bad-p106">The commands to create an event handler for the [ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) or [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) events are not available if the compatibility setting for the form template is set to **Web Browser Form**. This is because those events are not supported in the business logic of form templates published to document libraries on Microsoft SharePoint Server 2010 with InfoPath Forms Services. To create an event handler for the [ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) or [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) event, you must change the compatibility setting to **InfoPath Editor Form** in the InfoPath Designer. To do that, click the **File** tab, click **Form Options**, click **Compatibility**, and then set **Form type** to **InfoPath Editor Form**.</span></span> 
  
### <a name="add-an-event-handler-for-the-submit-event-of-a-form"></a><span data-ttu-id="b3bad-134">フォームの Submit イベントに対するイベント ハンドラーを追加する</span><span class="sxs-lookup"><span data-stu-id="b3bad-134">Add an event handler for the Submit event of a form</span></span>

1. <span data-ttu-id="b3bad-135">InfoPath Designer でフォーム テンプレートを開きます。</span><span class="sxs-lookup"><span data-stu-id="b3bad-135">Open the form template in the InfoPath Designer.</span></span>
    
2. <span data-ttu-id="b3bad-136">**[ファイル]** タブをクリックし、**[情報]** タブで **[送信先]** をクリックしてから、\*\* 送信オプション \*\* をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b3bad-136">Click the **File** tab, click **Submit To** on the **Info** tab, and then click \*\* Submit Options \*\*.</span></span>
    
3. <span data-ttu-id="b3bad-137">[ **ユーザーによるこのフォームの送信を許可する**] をクリックし、[ **コードを使用してユーザー設定操作を実行する**] をクリックし、[ **コードの編集**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b3bad-137">Click **Allow users to submit this form**, click **Perform custom action using Code**, and then click **Edit Code**.</span></span>
    
    <span data-ttu-id="b3bad-138">Visual Studio 2012 コード エディターの [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) イベントのスケルトン イベント ハンドラーにフォーカスが切り替わります。</span><span class="sxs-lookup"><span data-stu-id="b3bad-138">The focus switches to the skeleton event handler for the [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) event in the Visual Studio 2012 code editor.</span></span> 
    
### <a name="add-an-event-handler-for-the-save-event-of-a-form"></a><span data-ttu-id="b3bad-139">フォームの Save イベントに対するイベント ハンドラーを追加する</span><span class="sxs-lookup"><span data-stu-id="b3bad-139">Add an event handler for the Save event of a form</span></span>

1. <span data-ttu-id="b3bad-140">InfoPath Designer でフォーム テンプレートを開きます。</span><span class="sxs-lookup"><span data-stu-id="b3bad-140">Open the form template in the InfoPath Designer.</span></span>
    
2. <span data-ttu-id="b3bad-141">[ **ファイル**] タブをクリックして、[ **情報**] タブの [ **フォームのオプション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b3bad-141">Click the **File** tab, and then click **Form Options** on the **Info** tab.</span></span> 
    
3. <span data-ttu-id="b3bad-142">[ **保存**] カテゴリをクリックし、[ **ユーザー設定コードを使って保存**] チェック ボックスをオンにして [ **編集**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b3bad-142">Click the **Save** category, select the **Save using custom code** check box, and then click **Edit**.</span></span>
    
    <span data-ttu-id="b3bad-143">Visual Studio 2012 コード エディターの [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) イベントのスケルトン イベント ハンドラーにフォーカスが切り替わります。</span><span class="sxs-lookup"><span data-stu-id="b3bad-143">The focus switches to the skeleton event handler for the [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) event in the Visual Studio 2012 code editor.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="b3bad-p107">フォーム テンプレートの互換性設定が [ **InfoPath Forms Services**] に設定されている場合、[ **ユーザー設定コードを使って保存**] チェック ボックスは使用できません。これは、InfoPath Forms Services を実行する Microsoft SharePoint Server 2010 上のドキュメント ライブラリに発行されたフォーム テンプレートのビジネス ロジックでは、[Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) イベントがサポートされていないためです。 [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) イベントのイベント ハンドラーを作成するには、InfoPath Designer で互換性設定を [ **InfoPath エディター フォーム**] に変更する必要があります。これを行うには、[ **ファイル**] タブをクリックし、[ **フォームのオプション**]、[ **互換性**] の順にクリックして、[ **フォームの種類**] を [ **InfoPath エディター フォーム**] に設定します。</span><span class="sxs-lookup"><span data-stu-id="b3bad-p107">The **Save using custom code** check box is not available if the compatibility setting for the form template is set to **InfoPath Forms Services**. This is because the [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) event is not supported in the business logic of form templates published to document libraries on Microsoft SharePoint Server 2010 with InfoPath Forms Services. To create an event handler for the [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) event, you must change the compatibility setting to **InfoPath Editor Form** in the InfoPath Designer. To do that, click the **File** tab, click **Form Options**, click **Compatibility**, and then set **Form type** to **InfoPath Editor Form**.</span></span> 
  
### <a name="add-an-event-handler-for-the-versionupgrade-event-of-a-form"></a><span data-ttu-id="b3bad-148">フォームの VersionUpgrade イベントに対するイベント ハンドラーを追加する</span><span class="sxs-lookup"><span data-stu-id="b3bad-148">Add an event handler for the VersionUpgrade event of a form</span></span>

1. <span data-ttu-id="b3bad-149">InfoPath Designer でフォーム テンプレートを開きます。</span><span class="sxs-lookup"><span data-stu-id="b3bad-149">Open the form template in the InfoPath Designer.</span></span>
    
2. <span data-ttu-id="b3bad-150">[ **ファイル**] タブをクリックして、[ **情報**] タブの [ **フォームのオプション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b3bad-150">Click the **File** tab, and then click **Form Options** on the **Info** tab.</span></span> 
    
3. <span data-ttu-id="b3bad-151">[ **バージョン管理**] カテゴリをクリックし、[ **既存のフォームの更新**] ボックスの一覧の [ **ユーザー設定イベントの使用**] をクリックし、[ **編集**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b3bad-151">Click the **Versioning** category, select **Use custom event** in the **Update existing forms** drop-down box, and then click **Edit**.</span></span>
    
    <span data-ttu-id="b3bad-152">Visual Studio 2012 コード エディターの [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) イベントのスケルトン イベント ハンドラーにフォーカスが切り替わります。</span><span class="sxs-lookup"><span data-stu-id="b3bad-152">The focus switches to the skeleton event handler for the [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) event in the Visual Studio 2012 code editor.</span></span> 
    
### <a name="add-an-event-handler-for-the-merge-event-of-a-form"></a><span data-ttu-id="b3bad-153">フォームの Merge イベントに対するイベント ハンドラーを追加する</span><span class="sxs-lookup"><span data-stu-id="b3bad-153">Add an event handler for the Merge event of a form</span></span>

1. <span data-ttu-id="b3bad-154">InfoPath Designer でフォーム テンプレートを開きます。</span><span class="sxs-lookup"><span data-stu-id="b3bad-154">Open the form template in the InfoPath Designer.</span></span>
    
2. <span data-ttu-id="b3bad-155">[ **ファイル**] タブをクリックして、[ **情報**] タブの [ **フォームのオプション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b3bad-155">Click the **File** tab, and then click **Form Options** on the **Info** tab.</span></span> 
    
3. <span data-ttu-id="b3bad-156">[ **詳細設定**] カテゴリをクリックし、[ **フォームの結合を有効にする**] チェック ボックスをオンにし、[ **ユーザー設定コードを使って結合する**] チェック ボックスをオンにして、[ **編集**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b3bad-156">Click the **Advanced** category, click the **Enable form merging** check box, click the **Merge using custom code** check box, and then click **Edit**.</span></span>
    
    <span data-ttu-id="b3bad-157">Visual Studio 2012 コード エディターの [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) イベントのスケルトン イベント ハンドラーにフォーカスが切り替わります。</span><span class="sxs-lookup"><span data-stu-id="b3bad-157">The focus switches to the skeleton event handler for the [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) event in the Visual Studio 2012 code editor.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="b3bad-p108">フォーム テンプレートの互換性設定が [ **InfoPath Forms Services**] に設定されている場合、[ **フォームの結合を有効にする**] チェック ボックスは使用できません。これは、InfoPath Forms Services を実行する Microsoft SharePoint Server 2010 上のドキュメント ライブラリに発行されたフォーム テンプレートのビジネス ロジックでは、[Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) イベントがサポートされていないためです。 [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) イベントのイベント ハンドラーを作成するには、InfoPath Designer で互換性設定を [ **InfoPath エディター フォーム**] に変更する必要があります。これを行うには、[ **ファイル**] タブをクリックし、[ **フォームのオプション**]、[ **互換性**] の順にクリックして、[ **フォームの種類**] を [ **InfoPath エディター フォーム**] に設定します。</span><span class="sxs-lookup"><span data-stu-id="b3bad-p108">The **Enable form merging** check box is not available if the compatibility setting for the form template is set to **InfoPath Forms Services**. This is because the [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) event is not supported in the business logic of form templates published to document libraries on Microsoft SharePoint Server 2010 with InfoPath Forms Services. To create an event handler for the [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) event, you must change the compatibility setting to **InfoPath Editor Form** in the InfoPath Designer. To do that, click the **File** tab, click **Form Options**, click **Compatibility**, and then set **Form type** to **InfoPath Editor Form**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b3bad-162">関連項目</span><span class="sxs-lookup"><span data-stu-id="b3bad-162">See also</span></span>



[<span data-ttu-id="b3bad-163">チュートリアル: コードを含む基本的なフォーム テンプレートの作成</span><span class="sxs-lookup"><span data-stu-id="b3bad-163">Walkthrough: Creating a Basic Form Template with Code</span></span>](walkthrough-creating-a-basic-form-template-with-code.md)

