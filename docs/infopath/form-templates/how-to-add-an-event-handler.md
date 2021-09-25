---
title: イベント ハンドラーを追加する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- versionupgrade event [infopath 2007],handling events [InfoPath 2007],Changing event [InfoPath 2007],InfoPath 2007, adding event handlers,Changed event [InfoPath 2007],ContextChanged event [InfoPath 2007],Click event [InfoPath 2007],events [InfoPath 2007], adding event handlers,Sign event [InfoPath 2007],ViewSwitched event [InfoPath 2007],event handling [InfoPath 2007],Merge event [InfoPath 2007],Validating event [InfoPath 2007],Submit event [InfoPath 2007],Save event [InfoPath 2007],Loading event [InfoPath 2007]
ms.localizationpriority: medium
ms.assetid: d69393fb-fb5a-4edb-abc0-38f5d7e80bcc
description: このトピックでは、Visual Studio 2012 を使用して Microsoft InfoPath マネージ コード フォーム テンプレートにイベント ハンドラーを追加する手順を説明します。イベント ハンドラーをフォーム テンプレートに追加するには、まず、InfoPath Designer でフォーム テンプレートを開き、コードを記述するイベントに対して適切なユーザー インターフェイス コマンドを選択します。 InfoPath Designer でイベントのコマンドを選択したら、Visual Studio 2012 コード エディターのそのイベントのスケルトン イベント ハンドラーに自動的にフォーカスが切り替わります。
ms.openlocfilehash: bb94bc074c601dc215a72b7873992cb1891931d2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592880"
---
# <a name="add-an-event-handler"></a>イベント ハンドラーを追加する

このトピックでは、Visual Studio 2012 を使用して Microsoft InfoPath マネージ コード フォーム テンプレートにイベント ハンドラーを追加する手順を説明します。イベント ハンドラーをフォーム テンプレートに追加するには、まず、InfoPath Designer でフォーム テンプレートを開き、コードを記述するイベントに対して適切なユーザー インターフェイス コマンドを選択します。 InfoPath Designer でイベントのコマンドを選択したら、Visual Studio 2012 コード エディターのそのイベントのスケルトン イベント ハンドラーに自動的にフォーカスが切り替わります。
  
> [!IMPORTANT]
> イベント ハンドラーを追加するには、必ず、InfoPath Designer のユーザー インターフェイスを使用してください。このユーザー インターフェイスでイベント ハンドラーを追加すると、フォーム テンプレート プロジェクトの FormCode.cs または FormCode.vb ファイルの **InternalStartup** メソッドにイベント バインド コードが生成されます。 **InternalStartup** メソッドを作成したり、このメソッドに自分でコードを追加したりしないでください。 
  
### <a name="add-an-event-handler-for-the-click-event-of-a-button-control"></a>ボタン コントロールの Click イベントに対するイベント ハンドラーを追加する

1. InfoPath Designer でフォーム テンプレートを開き、フォームに **ボタン** コントロールを追加します。 
    
2. 追加したボタンをクリックし、リボンの [ **プロパティ**] タブの [ **ユーザー設定コード**] をクリックします。
    
    Visual Studio 2012 コード エディターの [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) イベントのスケルトン イベント ハンドラーにフォーカスが切り替わります。 
    
### <a name="add-an-event-handler-for-the-changing-validating-or-changed-event-of-a-field-or-group"></a>フィールドまたはグループの Changing、Validating、または Changed イベントに対するイベント ハンドラーを追加する

1. InfoPath Designer でフォーム テンプレートを開きます。
    
2. たとえば [ **テキスト ボックス**] コントロールなど、フィールドまたはグループにバインドされたデータ入力コントロールを右クリックします。 
    
3. [ **プログラミング**] をポイントし、イベント ハンドラーを作成するイベントをクリックします。Visual Studio 2012 コード エディターの [Changing](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changing.aspx) 、 [Validating](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Validating.aspx) 、または [Changed](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changed.aspx) イベントのスケルトン イベント ハンドラーにフォーカスが切り替わります。 
    
    > [!NOTE]
    > フォーム テンプレートの互換性設定が [ **Web ブラウザー フォーム**] に設定されている場合、 **Changing** イベントのイベント ハンドラーを作成するコマンドは使用できません。これは、InfoPath Forms Services を実行する Microsoft SharePoint Server 2010 上のドキュメント ライブラリに発行されたフォーム テンプレートのビジネス ロジックでは、 **Changing** イベントがサポートされていないためです。 **Changing** イベントのイベント ハンドラーを作成するには、InfoPath デザイン モードで互換性設定を [ **InfoPath エディター フォーム**] に変更する必要があります。これを行うには、[ **ファイル**] タブをクリックし、[ **フォームのオプション**]、[ **互換性**] の順にクリックして、[ **フォームの種類**] を [ **InfoPath エディター フォーム**] に設定します。 
  
### <a name="add-an-event-handler-for-the-loading-viewswitched-contextchanged-and-sign-events-of-a-form"></a>フォームの Loading、ViewSwitched、ContextChanged、および Sign イベントに対するイベント ハンドラーを追加する

1. InfoPath Designer でフォーム テンプレートを開きます。
    
2. リボンの [ **開発**] タブで、イベント ハンドラーを作成するフォーム イベントをクリックします。 
    
    Visual Studio 2012 コード エディターの [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) 、 [ViewSwitched](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ViewSwitched.aspx) 、 [ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) 、または [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) イベントのスケルトン イベント ハンドラーにフォーカスが切り替わります。 
    
    > [!NOTE]
    > フォーム テンプレートの互換性設定が [ [Web ブラウザー フォーム](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx)] に設定されている場合、[ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) または **Sign** イベントのイベント ハンドラーを作成するコマンドは使用できません。これは、InfoPath Forms Services を実行する Microsoft SharePoint Server 2010 上のドキュメント ライブラリに発行されたフォーム テンプレートのビジネス ロジックでは、それらのイベントがサポートされていないためです。 [ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) または [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) イベントのイベント ハンドラーを作成するには、InfoPath Designer で互換性設定を [ **InfoPath エディター フォーム**] に変更する必要があります。これを行うには、[ **ファイル**] タブをクリックし、[ **フォームのオプション**]、[ **互換性**] の順にクリックして、[ **フォームの種類**] を [ **InfoPath エディター フォーム**] に設定します。 
  
### <a name="add-an-event-handler-for-the-submit-event-of-a-form"></a>フォームの Submit イベントに対するイベント ハンドラーを追加する

1. InfoPath Designer でフォーム テンプレートを開きます。
    
2. **[ファイル]** タブをクリックし、**[情報]** タブで **[送信先]** をクリックしてから、** 送信オプション ** をクリックします。
    
3. [ **ユーザーによるこのフォームの送信を許可する**] をクリックし、[ **コードを使用してユーザー設定操作を実行する**] をクリックし、[ **コードの編集**] をクリックします。
    
    Visual Studio 2012 コード エディターの [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) イベントのスケルトン イベント ハンドラーにフォーカスが切り替わります。 
    
### <a name="add-an-event-handler-for-the-save-event-of-a-form"></a>フォームの Save イベントに対するイベント ハンドラーを追加する

1. InfoPath Designer でフォーム テンプレートを開きます。
    
2. [ **ファイル**] タブをクリックして、[ **情報**] タブの [ **フォームのオプション**] をクリックします。 
    
3. [ **保存**] カテゴリをクリックし、[ **ユーザー設定コードを使って保存**] チェック ボックスをオンにして [ **編集**] をクリックします。
    
    Visual Studio 2012 コード エディターの [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) イベントのスケルトン イベント ハンドラーにフォーカスが切り替わります。 
    
    > [!NOTE]
    > フォーム テンプレートの互換性設定が [ **InfoPath Forms Services**] に設定されている場合、[ **ユーザー設定コードを使って保存**] チェック ボックスは使用できません。これは、InfoPath Forms Services を実行する Microsoft SharePoint Server 2010 上のドキュメント ライブラリに発行されたフォーム テンプレートのビジネス ロジックでは、[Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) イベントがサポートされていないためです。 [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) イベントのイベント ハンドラーを作成するには、InfoPath Designer で互換性設定を [ **InfoPath エディター フォーム**] に変更する必要があります。これを行うには、[ **ファイル**] タブをクリックし、[ **フォームのオプション**]、[ **互換性**] の順にクリックして、[ **フォームの種類**] を [ **InfoPath エディター フォーム**] に設定します。 
  
### <a name="add-an-event-handler-for-the-versionupgrade-event-of-a-form"></a>フォームの VersionUpgrade イベントに対するイベント ハンドラーを追加する

1. InfoPath Designer でフォーム テンプレートを開きます。
    
2. [ **ファイル**] タブをクリックして、[ **情報**] タブの [ **フォームのオプション**] をクリックします。 
    
3. [ **バージョン管理**] カテゴリをクリックし、[ **既存のフォームの更新**] ボックスの一覧の [ **ユーザー設定イベントの使用**] をクリックし、[ **編集**] をクリックします。
    
    Visual Studio 2012 コード エディターの [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) イベントのスケルトン イベント ハンドラーにフォーカスが切り替わります。 
    
### <a name="add-an-event-handler-for-the-merge-event-of-a-form"></a>フォームの Merge イベントに対するイベント ハンドラーを追加する

1. InfoPath Designer でフォーム テンプレートを開きます。
    
2. [ **ファイル**] タブをクリックして、[ **情報**] タブの [ **フォームのオプション**] をクリックします。 
    
3. [ **詳細設定**] カテゴリをクリックし、[ **フォームの結合を有効にする**] チェック ボックスをオンにし、[ **ユーザー設定コードを使って結合する**] チェック ボックスをオンにして、[ **編集**] をクリックします。
    
    Visual Studio 2012 コード エディターの [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) イベントのスケルトン イベント ハンドラーにフォーカスが切り替わります。 
    
    > [!NOTE]
    > フォーム テンプレートの互換性設定が [ **InfoPath Forms Services**] に設定されている場合、[ **フォームの結合を有効にする**] チェック ボックスは使用できません。これは、InfoPath Forms Services を実行する Microsoft SharePoint Server 2010 上のドキュメント ライブラリに発行されたフォーム テンプレートのビジネス ロジックでは、[Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) イベントがサポートされていないためです。 [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) イベントのイベント ハンドラーを作成するには、InfoPath Designer で互換性設定を [ **InfoPath エディター フォーム**] に変更する必要があります。これを行うには、[ **ファイル**] タブをクリックし、[ **フォームのオプション**]、[ **互換性**] の順にクリックして、[ **フォームの種類**] を [ **InfoPath エディター フォーム**] に設定します。 
  
## <a name="see-also"></a>関連項目



[チュートリアル: コードを含む基本的なフォーム テンプレートの作成](walkthrough-creating-a-basic-form-template-with-code.md)

