---
title: InfoPath Forms Services で動作する InfoPath フォーム テンプレートを作成する
manager: soliver
ms.date: 03/20/2015
ms.audience: Developer
keywords:
- browser-compatible form templates [infopath 2007],forms [InfoPath 2007], browser-compatible,browser-compatible forms [InfoPath 2007],form templates [InfoPath 2007], browser-compatible,InfoPath 2007, browser-compatible forms,business logic, InfoPath Forms Services,InfoPath Forms Services, creating forms,InfoPath Forms Services, supported object model members,InfoPath Forms Services, supported classes and members
localization_priority: Normal
ms.assetid: 7bd4fbbb-49c6-46a1-9584-895e5aa9a772
description: Microsoft SharePoint Server 2013 と InfoPath Forms Services に展開されるブラウザー互換フォームでは、大部分の InfoPath フォーム使用シナリオで利用される機能とコントロールをサポートしています。しかし、InfoPath Forms Services で提供されるブラウザー互換フォームでは、InfoPath 機能をすべてサポートしているわけではありません。一部の機能とコントロールはサーバーに実装されません。また、サーバーには対応する機能がないこともあります。
ms.openlocfilehash: 65201358fc651325920bd3eefc863e839bb1f1a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799138"
---
# <a name="creating-infopath-form-templates-that-work-with-infopath-forms-services"></a>InfoPath Forms Services で動作する InfoPath フォーム テンプレートを作成する

Microsoft SharePoint Server 2013 と InfoPath Forms Services に展開されるブラウザー互換フォームでは、大部分の InfoPath フォーム使用シナリオで利用される機能とコントロールをサポートしています。しかし、InfoPath Forms Services で提供されるブラウザー互換フォームでは、InfoPath 機能をすべてサポートしているわけではありません。一部の機能とコントロールはサーバーに実装されません。また、サーバーには対応する機能がないこともあります。
  
ここでは、ブラウザー互換フォームでサポートされている機能、ブラウザー互換ーフォームで使用できない機能、およびブラウザー互換フォームで指定できるが Web ブラウザーで動作しない機能を示します。
  
## <a name="features-supported-by-both-infopath-and-infopath-forms-services"></a>InfoPath と InfoPath Forms Services の両方でサポートされている機能

ここでは、InfoPath Forms Services に展開され、InfoPath とブラウザーの両方で開くことができるブラウザー互換フォーム テンプレートでサポートされている機能の一覧を示します。
  
### <a name="controls"></a>コントロール

次のコントロールは、InfoPath とブラウザーの両方で開くことができるフォーム テンプレートでサポートされています。
  
- **テキスト ボックス**
    
- **リッチ テキスト ボックス**(Microsoft Internet Explorer でのみ編集可能) 
    
- **ドロップダウン リスト ボックス**
    
- **リスト ボックス**
    
- **日付の選択**(Internet Explorer 以外のブラウザーではテキスト ボックスとして表示される) 
    
- **チェック ボックスをオン**
    
- **オプション ボタン**
    
- **Button**
    
- **Section**
    
- **省略可能セクション**
    
- **繰り返しセクション**
    
- **繰り返しテーブル**
    
- **添付ファイル**
    
- **Hyperlink**
    
- **式ボックス**
    
- **コンボ ボックス**
    
- **複数選択リスト ボックス**
    
- **箇条書きのリスト**
    
- **番号付きリスト**
    
- **標準リスト**
    
- **Picture**
    
- **選択肢グループ**
    
- **選択肢セクション**
    
- **ユーザー/グループの選択**
    
- **外部アイテム ピッカー**
    
- **ピクチャ ボタン**
    
- **計算値**
    
### <a name="declarative-features"></a>宣言機能

InfoPath とブラウザーの両方で動作する他の宣言機能は以下のとおりです。
  
- ルール
    
- 計算
    
- 検証
    
> [!NOTE]
> [!メモ] 簡単なルール、計算、およびデータ検証は、JScript を使用してブラウザーで有効にし、実行されます。複雑なルール、計算、およびデータ検証はサーバーで行うため、これらの操作にポストバックが必要です。 
  
### <a name="code"></a>コード

ビジネス ロジック コードは、[Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) 名前空間によって提供される InfoPath マネージ コード オブジェクト モデルに基づく必要があります。サーバーで実行されるビジネス ロジック コードには、次の制限が適用されます。 
  
- 各サーバー要求は異なるフロントエンドで処理されることがあり、InfoPath Forms Services ではビジネス ロジックの 1 つのインスタンスしか読み込まないため、プログラマはグローバル変数または静的変数に代入されたデータに依存することはできません。この問題に対処するために、ビジネス ロジックでは状態をプロパティ バッグに格納し、[FormState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.FormState.aspx) プロパティによって提供されるものにアクセスする必要があります。 
    
- **Microsoft.Office.InfoPath** 名前空間のメンバーのサブセットでは、サーバーでサポートされない Information Rights Management (IRM) などの機能が提供されます。サポートされているオブジェクト モデル メンバーとサポートされていないメンバーについては、このトピックの「InfoPath と InfoPath Forms Services で動作するオブジェクト モデル メンバー」と「InfoPath でのみ動作するオブジェクト モデル メンバー」を参照してください。 
    
- VBScript、JScript、および [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) 名前空間のメンバーによって提供される InfoPath 2003 互換オブジェクト モデルで作成されたビジネス ロジックはサーバーではサポートされません。 
    
## <a name="features-not-supported-by-infopath-forms-services"></a>InfoPath Forms Services でサポートされていない機能

ここでは、InfoPath Forms Services に展開され、InfoPath とブラウザーの両方で開くことができるブラウザー互換フォーム テンプレートではサポートされていない機能の一覧を示します。
  
InfoPath デザイン モードで **デザイン チェック**機能を使用し、InfoPath Forms Services との互換性を確認すると、サポートされていない機能ではエラーが発生するかメッセージが表示されます。エラーが発生する機能があると、フォーム テンプレートはブラウザー対応フォームとして発行できません。メッセージが表示される機能は使用できますが、フォームがブラウザーで開かれるとき、その機能は実行されません。 
  
### <a name="controls"></a>コントロール

次のコントロールとコントロール機能は、InfoPath とブラウザーの両方で開くことができるフォーム テンプレートではサポートされません。
  
- 繰り返しコントロールに対するフィルター
    
- **マスター/詳細**
    
- **縦書きラベル**
    
- **横方向繰り返しテーブル**
    
- **インク描画**
    
- **繰り返し再帰セクション**
    
### <a name="other-features-that-are-not-supported-or-not-fully-supported-by-infopath-forms-services"></a>InfoPath Forms Services でサポートされていないか完全にはサポートされていない他の機能

InfoPath Forms Services ではサポートされていない他の機能
  
- ActiveX コントロール。
    
- HTML 作業ウィンドウ。
    
- コントロールのプレースホルダー テキスト。たとえば、"テキストを入力するにはここをクリックします" (ブラウザーにテキストは表示されません)。
    
- データベース データ接続は SQL サーバー データベースへの読み取り専用アクセスに制限されます。
    
- ユーザー ロール。
    
- オブジェクト モデルによるデジタル署名拡張。サーバーでのデジタル署名は Microsoft Internet Explorer でのみ実行される ActiveX コントロールによってサポートされます。
    
- Human Workflow Services (HWS) 統合。HWS は BizTalk Server で現在使用されていません。
    
- XML スキーマ エラー メッセージのオーバーライド。この機能はあまり使用されません。ドキュメントが検証されないとき (通常は種類の不一致のため)、フォーム設計者はこの機能を使用し、MSXML または **System.Xml** で提供されているメッセージとは異なるメッセージを指定できます。この機能はデザイン モード ユーザー インターフェイスではサポートされていないため、フォーム定義 (.xsf) ファイルを手動で編集する必要があります。 
    
### <a name="features-with-no-direct-parallel-on-the-infopath-forms-services"></a>InfoPath Forms Services に直接対応するものがない機能

InfoPath Forms Services ではサポートされていない他の機能
  
- モードレス検証中のポップアップ ダイアログ
    
- Outlook 統合
    
- COM アドイン
    
- フォームの結合
    
- 自動保存、クラッシュの検出、および回復
    
- メールの封筒
    
- Excel へのエクスポート
    
- タブレット/インク機能の**インク描画**コントロールを含む 
    
- 元に戻す/やり直す
    
- Information Rights Management (IRM)
    
- ビジネス ロジックからのモーダル ダイアログ
    
- XSLT の拡張機能 (**xd:preserve**ブロック) 
    
- 外部自動化
    
- オフライン クエリ キャッシュ
    
- スペルチェック
    
- 制限セキュリティ モード
    
> [!NOTE]
> [!メモ] InfoPath デザインモードの **デザイン チェック**機能を使用したとき、上記の機能にはエラーやメッセージ通知は発生しません。 
  
## <a name="object-model-members-that-work-in-both-infopath-and-infopath-forms-services"></a>InfoPath と InfoPath Forms Services の両方で動作するオブジェクト モデル メンバー

InfoPath は、新しいマネージ コード オブジェクト モデルと、フォーム テンプレート内でカスタム ビジネス ロジックを作成するための機能のコア セットを提供します。この新しいオブジェクト モデルを使用して作成したビジネス ロジックを、InfoPath Forms Services を使用する SharePoint Server 2010 に展開した場合、Web ブラウザーでも InfoPath でも実行することができます。また、InfoPath で編集のために開かれたフォーム テンプレート内でのみ実行できる、このオブジェクト モデルで提供される追加レベルの機能を使用するビジネス ロジックを作成することもできます。
  
フォームが Web ブラウザーと InfoPath の両方で開かれたときに実行されるビジネス ロジックを書くには、新しいフォーム テンプレートを作成する際に、[ **フォーム テンプレートのデザイン**] ダイアログ ボックスで [ **ブラウザー互換の機能のみを有効にする**] チェック ボックスをオンにします。InfoPath で開かれたときにのみ追加機能を使用できるビジネス ロジックを書くには、新しいフォーム テンプレートを作成する際に [ **ブラウザー互換の機能のみを有効にする**] チェック ボックスをオフにします。この設定は、フォーム テンプレートの作成後に変更することができます。変更するには、[ **デザイン チェック**] 作業ウィンドウで [ **互換性設定の変更**] をクリックし、[ **ブラウザーまたは InfoPath で開くことができるフォーム テンプレートをデザインする**] チェック ボックスをオンまたはオフにします。ブラウザー互換フォーム テンプレートを作成する場合、InfoPath Forms Services と互換性のないクラスまたはメンバーを使用すると、コンパイラでエラーが表示されます。 
  
> [!NOTE]
> [!メモ] マネージ コードが入ったブラウザー対応フォーム テンプレートは、InfoPath Forms Services を使用する SharePoint Server 2010、または共有の場所に発行した後、そのフォーム テンプレートをアップロードし、サーバー管理者の承認を受けた後、実行できるようになります。 
  
[Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) 名前空間によって提供される InfoPath マネージ コード オブジェクト モデルの次のクラスとメンバーは、InfoPath と InfoPath Forms Services の両方でサポートされています。 
  
|**親クラス**|**メンバー**|
|:-----|:-----|
|[AdoQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.aspx) <br/> |[BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.BuildSqlFromXmlNodes.aspx) <br/> |
||[Command](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.Command.aspx) <br/> |
||[Connection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.Connection.aspx) <br/> |
||[Timeout](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.Timeout.aspx) <br/> |
||[BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.BuildSqlFromXmlNodes.aspx) <br/> |
||[Command](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.Command.aspx) <br/> |
||[Connection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.Connection.aspx) <br/> |
||[Timeout](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.Timeout.aspx) <br/> |
|[Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) <br/> |[Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Environment.aspx) <br/> |
||[Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Name.aspx) <br/> |
||[User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.User.aspx) <br/> |
|[ButtonEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.aspx) <br/> |[Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) <br/> |
|[ClickedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.aspx) <br/> |[ControlId](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.ControlId.aspx) <br/> |
||[Source](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.Source.aspx) <br/> |
|[イベント コントロール](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ControlEvents.aspx) <br/> |[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ControlEvents.Item.aspx) <br/> |
|[DataConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnection.aspx) <br/> |[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnection.Execute.aspx) <br/> |
||[Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnection.Name.aspx) <br/> |
|[DataConnectionCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnectionCollection.aspx) <br/> |[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnectionCollection.Count.aspx) <br/> |
||[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnectionCollection.GetEnumerator.aspx) <br/> |
||[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnectionCollection.Item.aspx) <br/> |
||[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnectionCollection.Item.aspx) <br/> |
|[データ ソース](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) <br/> |[CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) <br/> |
||[GetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.GetNamedNodeProperty.aspx) <br/> |
||[Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.Name.aspx) <br/> |
||[QueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.QueryConnection.aspx) <br/> |
||[ReadOnly](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.ReadOnly.aspx) <br/> |
||[SetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.SetNamedNodeProperty.aspx) <br/> |
|[DataSourceCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) <br/> |[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Count.aspx) <br/> |
||[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.GetEnumerator.aspx) <br/> |
||[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Item.aspx) <br/> |
||[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Item.aspx) <br/> |
|[EmailAttachmentType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailAttachmentType.aspx) <br/> |[None](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailAttachmentType.None.aspx) <br/> |
||[Xml](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailAttachmentType.Xml.aspx) <br/> |
||[XmlXsn](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailAttachmentType.XmlXsn.aspx) <br/> |
|[EmailSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.aspx) <br/> |[AttachmentFileName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.AttachmentFileName.aspx) <br/> |
||[Bcc](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.Bcc.aspx) <br/> |
||[CC](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.CC.aspx) <br/> |
||[EmailAttachmentType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.EmailAttachmentType.aspx) <br/> |
||[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.Execute.aspx) <br/> |
||[Introduction](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.Introduction.aspx) <br/> |
||[Subject](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.Subject.aspx) <br/> |
||[To](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.To.aspx) <br/> |
|[Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) <br/> |[IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) <br/> |
||[IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) <br/> |
|[EventManager](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EventManager.aspx) <br/> |[イベント コントロール](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EventManager.ControlEvents.aspx) <br/> |
||[FormEvents](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EventManager.FormEvents.aspx) <br/> |
||[XmlEvents](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EventManager.XmlEvents.aspx) <br/> |
|[FileQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.aspx) <br/> |[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.Execute.aspx) <br/> |
||[FileLocation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.FileLocation.aspx) <br/> |
|[FileSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.aspx) <br/> |[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.Execute.aspx) <br/> |
||[Filename](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.Filename.aspx) <br/> |
||[FolderUrl](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.FolderUrl.aspx) <br/> |
|[FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) <br/> |[DetailedMessage](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.DetailedMessage.aspx) <br/> |
||[FormErrorType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.FormErrorType.aspx) <br/> |
||[Message](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Message.aspx) <br/> |
||[Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Name.aspx) <br/> |
||[Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Site.aspx) <br/> |
|[FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) <br/> |[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) <br/> |
||[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) <br/> |
||[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Count.aspx) <br/> |
||[Delete](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Delete.aspx) <br/> |
||[Delete](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Delete.aspx) <br/> |
||[DeleteAll](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.DeleteAll.aspx) <br/> |
||[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.GetEnumerator.aspx) <br/> |
||[GetErrors](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.GetErrors.aspx) <br/> |
||[GetErrors](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.GetErrors.aspx) <br/> |
||[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Item.aspx) <br/> |
|[FormErrorType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorType.aspx) <br/> |[SchemaValidation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorType.SchemaValidation.aspx) <br/> |
||[SystemGenerated](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorType.SystemGenerated.aspx) <br/> |
||[ユーザー定義](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorType.UserDefined.aspx) <br/> |
|[FormEvents](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.aspx) <br/> |[Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) <br/> |
||[Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) <br/> |
||[VersionUpgrade](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.VersionUpgrade.aspx) <br/> |
||[ViewSwitched](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ViewSwitched.aspx) <br/> |
|[FormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) <br/> |[Manifest](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Manifest.aspx) <br/> |
||[OpenFileFromPackage](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.OpenFileFromPackage.aspx) <br/> |
||[Uri](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Uri.aspx) <br/> |
||[Version](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Version.aspx) <br/> |
|[LoadingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.LoadingEventArgs.aspx) <br/> |[CancelableArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.LoadingEventArgs.CancelableArgs.aspx) <br/> |
||[InputParameters](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.LoadingEventArgs.InputParameters.aspx) <br/> |
||[SetDefaultView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.LoadingEventArgs.SetDefaultView.aspx) <br/> |
||[SetDefaultView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.LoadingEventArgs.SetDefaultView.aspx) <br/> |
|[SharepointListQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.aspx) <br/> |[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.Execute.aspx) <br/> |
||[QueryThisFormOnly](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.QueryThisFormOnly.aspx) <br/> |
||[SiteUrl](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.SiteUrl.aspx) <br/> |
|[SubmitEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SubmitEventArgs.aspx) <br/> |[CancelableArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SubmitEventArgs.CancelableArgs.aspx) <br/> |
|[User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) <br/> |[ログイン名が表示](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.LoginName.aspx) <br/> |
||[UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) <br/> |
|[VersionUpgradeEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.VersionUpgradeEventArgs.aspx) <br/> |[CancelableArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.VersionUpgradeEventArgs.CancelableArgs.aspx) <br/> |
||[DocumentVersion](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.VersionUpgradeEventArgs.DocumentVersion.aspx) <br/> |
||[FormTemplateVersion](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.VersionUpgradeEventArgs.FormTemplateVersion.aspx) <br/> |
|[View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) <br/> |[ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ViewInfo.aspx) <br/> |
|[ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) <br/> |[Caption](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.Caption.aspx) <br/> |
||[Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.Name.aspx) <br/> |
|[ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) <br/> |[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Count.aspx) <br/> |
||[Default](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Default.aspx) <br/> |
||[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.GetEnumerator.aspx) <br/> |
||[Initial](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Initial.aspx) <br/> |
||[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Item.aspx) <br/> |
||[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Item.aspx) <br/> |
||[SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.SwitchView.aspx) <br/> |
||[SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.SwitchView.aspx) <br/> |
|[WebServiceConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.aspx) <br/> |[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.Execute.aspx) <br/> |
||[GenerateDataSetDiffGram](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.GenerateDataSetDiffGram.aspx) <br/> |
||[ServiceUrl](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.ServiceUrl.aspx) <br/> |
||[SoapAction](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.SoapAction.aspx) <br/> |
||[Timeout](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.Timeout.aspx) <br/> |
||[WsdlUrl](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.WsdlUrl.aspx) <br/> |
|[XmlEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.aspx) <br/> |[Changed](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changed.aspx) <br/> |
||[RaiseUndoRedoForChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.RaiseUndoRedoForChanged.aspx) <br/> |
||[Validating](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Validating.aspx) <br/> |
|[XmlEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) <br/> |[Match](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Match.aspx) <br/> |
||[新しい値](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.NewValue.aspx) <br/> |
||[OldParent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.OldParent.aspx) <br/> |
||[OldValue](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.OldValue.aspx) <br/> |
||[Operation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Operation.aspx) <br/> |
||[Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Site.aspx) <br/> |
||[に](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.UndoRedo.aspx) <br/> |
|[XmlEvents](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvents.aspx) <br/> |[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvents.Item.aspx) <br/> |
||[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvents.Item.aspx) <br/> |
|[XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) <br/> |[CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) <br/> |
||[DataConnections](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataConnections.aspx) <br/> |
||[データ ソース](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) <br/> |
||[Errors](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Errors.aspx) <br/> |
||[FormState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.FormState.aspx) <br/> |
||[MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) <br/> |
||[ネーム スペース マネージャー](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NamespaceManager.aspx) <br/> |
||[New](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.New.aspx) <br/> |
||[NotifyHost](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NotifyHost.aspx) <br/> |
||[QueryDataConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.QueryDataConnection.aspx) <br/> |
||[ReadOnly](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ReadOnly.aspx) <br/> |
||[Signed](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Signed.aspx) <br/> |
||[Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Submit.aspx) <br/> |
||[Template](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Template.aspx) <br/> |
||[Uri](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Uri.aspx) <br/> |
||[ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx) <br/> |
||[XmlLang](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.XmlLang.aspx) <br/> |
|[XmlFormCancelEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCancelEventArgs.aspx) <br/> |[Message](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCancelEventArgs.Message.aspx) <br/> |
||[MessageDetails](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCancelEventArgs.MessageDetails.aspx) <br/> |
|[XmlOperation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlOperation.aspx) <br/> |[Delete](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlOperation.Delete.aspx) <br/> |
||[Insert](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlOperation.Insert.aspx) <br/> |
||[None](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlOperation.None.aspx) <br/> |
||[「Valuechange」](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlOperation.ValueChange.aspx) <br/> |
|[XmlValidatingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) <br/> |[ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) <br/> |
||[ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) <br/> |
||[ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) <br/> |
|[XPathTypedValue](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XPathTypedValue.aspx) <br/> |[Evaluate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XPathTypedValue.Evaluate.aspx) <br/> |
||[SetStringValue](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XPathTypedValue.SetStringValue.aspx) <br/> |
||[ToString](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XPathTypedValue.ToString.aspx) <br/> |
||[XPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XPathTypedValue.XPath.aspx) <br/> |
   
## <a name="object-model-members-that-work-only-in-infopath"></a>InfoPath でのみ動作するオブジェクト モデル メンバー

[Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) 名前空間によって提供される InfoPath マネージ コード オブジェクト モデルの次のクラスとメンバーは InfoPath でのみサポートされています。 
  
> [!NOTE]
> [!メモ] フォームをブラウザーで開くか InfoPath で開くかを指定する条件付きロジックを書く場合、次のオブジェクト モデル メンバーはブラウザー対応のフォーム テンプレートのコードで使用できます。 詳細については、[実行時環境を決定する条件付きロジックを記述](how-to-write-conditional-logic-that-determines-the-run-time-environment.md)を参照してください。 
  
|**親クラス**|**メンバー**|
|:-----|:-----|
|[ファイアウォール](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.aspx) <br/> |[Copy](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.Copy.aspx) <br/> |
||[Cut](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.Cut.aspx) <br/> |
||[Delete](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.Delete.aspx) <br/> |
||[Paste](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.Paste.aspx) <br/> |
||[XCollectionInsert](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XCollectionInsert.aspx) <br/> |
||[XCollectionInsertAfter](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XCollectionInsertAfter.aspx) <br/> |
||[XCollectionInsertBefore](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XCollectionInsertBefore.aspx) <br/> |
||[XCollectionRefreshFilter](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XCollectionRefreshFilter.aspx) <br/> |
||[XCollectionRemove](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XCollectionRemove.aspx) <br/> |
||[XCollectionRemoveAll](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XCollectionRemoveAll.aspx) <br/> |
||[XFileAttachmentAttach](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XFileAttachmentAttach.aspx) <br/> |
||[XFileAttachmentOpen](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XFileAttachmentOpen.aspx) <br/> |
||[XFileAttachmentRemove](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XFileAttachmentRemove.aspx) <br/> |
||[XFileAttachmentSaveAs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XFileAttachmentSaveAs.aspx) <br/> |
||[XOptionalInsert](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XOptionalInsert.aspx) <br/> |
||[XOptionalRemove](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XOptionalRemove.aspx) <br/> |
||[XReplaceReplace](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XReplaceReplace.aspx) <br/> |
|[Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) <br/> |[ActiveWindow](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.ActiveWindow.aspx) <br/> |
||[CacheFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.CacheFormTemplate.aspx) <br/> |
||[ComAddIns](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.ComAddIns.aspx) <br/> |
||[GetFormTemplateLocation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.GetFormTemplateLocation.aspx) <br/> |
||[IsDestinationReachable](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.IsDestinationReachable.aspx) <br/> |
||[LanguageSettings](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.LanguageSettings.aspx) <br/> |
||[MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.MachineOnlineState.aspx) <br/> |
||[Quit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Quit.aspx) <br/> |
||[Quit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Quit.aspx) <br/> |
||[RegisterFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.RegisterFormTemplate.aspx) <br/> |
||[RegisterFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.RegisterFormTemplate.aspx) <br/> |
||[UnregisterFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.UnregisterFormTemplate.aspx) <br/> |
||[UsableHeight](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.UsableHeight.aspx) <br/> |
||[UsableWidth](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.UsableWidth.aspx) <br/> |
||[Version](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Version.aspx) <br/> |
||[Windows](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Windows.aspx) <br/> |
||[XmlForms](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.XmlForms.aspx) <br/> |
|[Certificate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Certificate.aspx) <br/> |[できます。](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Certificate.ExpirationDate.aspx) <br/> |
||[IssuedBy](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Certificate.IssuedBy.aspx) <br/> |
||[IssuedTo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Certificate.IssuedTo.aspx) <br/> |
||[Status](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Certificate.Status.aspx) <br/> |
|[CertificateStatus](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.CertificateStatus.aspx) <br/> |[Error](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.CertificateStatus.Error.aspx) <br/> |
||[Expired](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.CertificateStatus.Expired.aspx) <br/> |
||[NotTrusted](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.CertificateStatus.NotTrusted.aspx) <br/> |
||[Revoked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.CertificateStatus.Revoked.aspx) <br/> |
||[Valid](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.CertificateStatus.Valid.aspx) <br/> |
|[ContextChangedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.aspx) <br/> |[ChangeType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.ChangeType.aspx) <br/> |
||[Context](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.Context.aspx) <br/> |
||[に](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.UndoRedo.aspx) <br/> |
|[ErrorMode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ErrorMode.aspx) <br/> |[Modal](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ErrorMode.Modal.aspx) <br/> |
||[Modeless](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ErrorMode.Modeless.aspx) <br/> |
|[ExportFormat](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ExportFormat.aspx) <br/> |[Mht](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ExportFormat.Mht.aspx) <br/> |
||[Pdf](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ExportFormat.Pdf.aspx) <br/> |
||[Xps](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ExportFormat.Xps.aspx) <br/> |
|[FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) <br/> |[エラー コード](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.ErrorCode.aspx) <br/> |
|[FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) <br/> |[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) <br/> |
||[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) <br/> |
|[FormEvents](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.aspx) <br/> |[ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) <br/> |
||[Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) <br/> |
||[Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) <br/> |
||[Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) <br/> |
|[FormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) <br/> |[CacheId](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.CacheId.aspx) <br/> |
|[HtmlTaskPane](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.HtmlTaskPane.aspx) <br/> |[HtmlDocument](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.HtmlTaskPane.HtmlDocument.aspx) <br/> |
||[HtmlWindow](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.HtmlTaskPane.HtmlWindow.aspx) <br/> |
||[Navigate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.HtmlTaskPane.Navigate.aspx) <br/> |
|[MachineState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MachineState.aspx) <br/> |[IEInOfflineState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MachineState.IEInOfflineState.aspx) <br/> |
||[Offline](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MachineState.Offline.aspx) <br/> |
||[Online](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MachineState.Online.aspx) <br/> |
|[MailEnvelope](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.aspx) <br/> |[Available](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.Available.aspx) <br/> |
||[Bcc](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.Bcc.aspx) <br/> |
||[CC](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.CC.aspx) <br/> |
||[EmailAttachmentType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.EmailAttachmentType.aspx) <br/> |
||[Introduction](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.Introduction.aspx) <br/> |
||[Subject](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.Subject.aspx) <br/> |
||[To](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.To.aspx) <br/> |
||[Visible](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.Visible.aspx) <br/> |
|[MergeEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.aspx) <br/> |[CancelableArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.CancelableArgs.aspx) <br/> |
||[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.Count.aspx) <br/> |
||[Index](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.Index.aspx) <br/> |
||[Rollback](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.Rollback.aspx) <br/> |
||[Xml](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.Xml.aspx) <br/> |
|[Permission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.aspx) <br/> |[管理用](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.ApplyPolicy.aspx) <br/> |
||[DocumentAuthor](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.DocumentAuthor.aspx) <br/> |
||[Enabled](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.Enabled.aspx) <br/> |
||[管理](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.PermissionFromPolicy.aspx) <br/> |
||[許可](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.PolicyDescription.aspx) <br/> |
||[グループ](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.PolicyName.aspx) <br/> |
||[RequestPermissionUrl](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.RequestPermissionUrl.aspx) <br/> |
||[StoreLicenses](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.StoreLicenses.aspx) <br/> |
||[UserPermissions](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.UserPermissions.aspx) <br/> |
|[PermissionType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.aspx) <br/> |[Change](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.Change.aspx) <br/> |
||[Edit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.Edit.aspx) <br/> |
||[Extract](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.Extract.aspx) <br/> |
||[FullControl](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.FullControl.aspx) <br/> |
||[ObjectModel](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.ObjectModel.aspx) <br/> |
||[Print](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.Print.aspx) <br/> |
||[Read](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.Read.aspx) <br/> |
||[Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.Save.aspx) <br/> |
||[View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.View.aspx) <br/> |
|[SaveEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SaveEventArgs.aspx) <br/> |[CancelableArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SaveEventArgs.CancelableArgs.aspx) <br/> |
||[CloseIfSaveCancelled](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SaveCancelEventArgs.CloseIfSaveCancelled.aspx) <br/> |
||[Filename](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SaveEventArgs.Filename.aspx) <br/> |
||[IsSaveAs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SaveEventArgs.IsSaveAs.aspx) <br/> |
||[PerformSaveOperation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SaveEventArgs.PerformSaveOperation.aspx) <br/> |
|[Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) <br/> |[Certificate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Certificate.aspx) <br/> |
||[Comment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Comment.aspx) <br/> |
||[Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) <br/> |
||[SignatureBlockXmlNode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.SignatureBlockXmlNode.aspx) <br/> |
||[Status](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Status.aspx) <br/> |
|[SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) <br/> |[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.Count.aspx) <br/> |
||[CreateSignature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.CreateSignature.aspx) <br/> |
||[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.GetEnumerator.aspx) <br/> |
||[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.Item.aspx) <br/> |
|[SignatureRelation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureRelation.aspx) <br/> |[Cosign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureRelation.Cosign.aspx) <br/> |
||[副](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureRelation.CounterSign.aspx) <br/> |
||[Single](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureRelation.Single.aspx) <br/> |
|[SignatureStatus](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureStatus.aspx) <br/> |[Error](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureStatus.Error.aspx) <br/> |
||[Invalid](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureStatus.Invalid.aspx) <br/> |
||[Unsupported](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureStatus.Unsupported.aspx) <br/> |
||[Valid](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureStatus.Valid.aspx) <br/> |
|[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) <br/> |[Caption](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Caption.aspx) <br/> |
||[Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Name.aspx) <br/> |
||[Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Sign.aspx) <br/> |
||[SignatureContainer](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.SignatureContainer.aspx) <br/> |
||[SignatureRelation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.SignatureRelation.aspx) <br/> |
||[Signatures](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Signatures.aspx) <br/> |
||[XPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.XPath.aspx) <br/> |
|[SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) <br/> |[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.Count.aspx) <br/> |
||[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.GetEnumerator.aspx) <br/> |
||[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.Item.aspx) <br/> |
||[ShowSignatureDialog](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.ShowSignatureDialog.aspx) <br/> |
|[SignEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.aspx) <br/> |[SignatureWizard](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.SignatureWizard.aspx) <br/> |
||[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.SignedDataBlock.aspx) <br/> |
|[作業ウィンドウ](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPane.aspx) <br/> |[TaskPaneType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPane.TaskPaneType.aspx) <br/> |
||[Visible](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPane.Visible.aspx) <br/> |
|[TaskPaneCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneCollection.aspx) <br/> |[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneCollection.Count.aspx) <br/> |
||[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneCollection.GetEnumerator.aspx) <br/> |
||[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneCollection.Item.aspx) <br/> |
||[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneCollection.Item.aspx) <br/> |
|[TaskPaneType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneType.aspx) <br/> |[BulletsNumbering](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneType.BulletsNumbering.aspx) <br/> |
||[クリップアート](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneType.ClipArt.aspx) <br/> |
||[Find](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneType.Find.aspx) <br/> |
||[Formatting](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneType.Formatting.aspx) <br/> |
||[Html](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneType.Html.aspx) <br/> |
||[ParagraphFormatting](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneType.ParagraphFormatting.aspx) <br/> |
||[Replace](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneType.Replace.aspx) <br/> |
||[Spelling](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneType.Spelling.aspx) <br/> |
|[User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) <br/> |[IsUserMemberOf](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.IsUserMemberOf.aspx) <br/> |
|[UserPermission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.aspx) <br/> |[できます。](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.ExpirationDate.aspx) <br/> |
||[Permission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.Permission.aspx) <br/> |
||[Remove](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.Remove.aspx) <br/> |
||[ユーザー Id](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.UserId.aspx) <br/> |
|[UserPermissionCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.aspx) <br/> |[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Add.aspx) <br/> |
||[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Add.aspx) <br/> |
||[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Add.aspx) <br/> |
||[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Add.aspx) <br/> |
||[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Count.aspx) <br/> |
||[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.GetEnumerator.aspx) <br/> |
||[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Item.aspx) <br/> |
||[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Item.aspx) <br/> |
||[Remove](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Remove.aspx) <br/> |
||[一括削除](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.RemoveAll.aspx) <br/> |
|[View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) <br/> |[DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.DisableAutoUpdate.aspx) <br/> |
||[EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.EnableAutoUpdate.aspx) <br/> |
||[ExecuteAction](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx) <br/> |
||[ExecuteAction](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx) <br/> |
||[Export](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Export.aspx) <br/> |
||[ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ForceUpdate.aspx) <br/> |
||[GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) <br/> |
||[GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) <br/> |
||[GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx) <br/> |
||[SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) <br/> |
||[SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) <br/> |
||[SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) <br/> |
||[SelectText](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) <br/> |
||[SelectText](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) <br/> |
||[ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ShowMailItem.aspx) <br/> |
||[Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx) <br/> |
|[ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) <br/> |[HideName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.HideName.aspx) <br/> |
|[Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) <br/> |[Activate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Activate.aspx) <br/> |
||[Active](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Active.aspx) <br/> |
||[Caption](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Caption.aspx) <br/> |
||[Close](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Close.aspx) <br/> |
||[Close](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Close.aspx) <br/> |
||[CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) <br/> |
||[Height](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Height.aspx) <br/> |
||[Left](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Left.aspx) <br/> |
||[MailEnvelope](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.MailEnvelope.aspx) <br/> |
||[TaskPanes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.TaskPanes.aspx) <br/> |
||[Top](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Top.aspx) <br/> |
||[Width](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Width.aspx) <br/> |
||[WindowState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.WindowState.aspx) <br/> |
||[サービス クラス](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.WindowType.aspx) <br/> |
||[XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.XmlForm.aspx) <br/> |
|[WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) <br/> |[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.Count.aspx) <br/> |
||[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.GetEnumerator.aspx) <br/> |
||[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.Item.aspx) <br/> |
|[WindowState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowState.aspx) <br/> |[Maximized](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowState.Maximized.aspx) <br/> |
||[Minimized](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowState.Minimized.aspx) <br/> |
||[Normal](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowState.Normal.aspx) <br/> |
|[サービス クラス](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowType.aspx) <br/> |[Designer](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowType.Designer.aspx) <br/> |
||[Editor](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowType.Editor.aspx) <br/> |
|[XmlChangingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlChangingEventArgs.aspx) <br/> |[CancelableArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlChangingEventArgs.CancelableArgs.aspx) <br/> |
|[XmlEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.aspx) <br/> |[Changing](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changing.aspx) <br/> |
|[XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) <br/> |[Close](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Close.aspx) <br/> |
||[Dirty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Dirty.aspx) <br/> |
||[Extension](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Extension.aspx) <br/> |
||[GetWorkflowTasks](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.GetWorkflowTasks.aspx) <br/> |
||[GetWorkflowTemplates](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.GetWorkflowTemplates.aspx) <br/> |
||[Host](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Host.aspx) <br/> |
||[Hosted](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Hosted.aspx) <br/> |
||[ホスト名](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.HostName.aspx) <br/> |
||[MergeForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx) <br/> |
||[MergeForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx) <br/> |
||[Permission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Permission.aspx) <br/> |
||[Print](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Print.aspx) <br/> |
||[Print](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Print.aspx) <br/> |
||[Recovered](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Recovered.aspx) <br/> |
||[Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Save.aspx) <br/> |
||[SaveAs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SaveAs.aspx) <br/> |
||[SetSaveAsDialogFilename](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SetSaveAsDialogFilename.aspx) <br/> |
||[SetSaveAsDialogLocation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SetSaveAsDialogLocation.aspx) <br/> |
||[SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SignedDataBlocks.aspx) <br/> |
||[TaskPanes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.TaskPanes.aspx) <br/> |
||[UserRole](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.UserRole.aspx) <br/> |
|[XmlFormCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) <br/> |[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Count.aspx) <br/> |
|[XmlFormCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) <br/> |[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.GetEnumerator.aspx) <br/> |
||[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Item.aspx) <br/> |
||[New](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.New.aspx) <br/> |
||[New](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.New.aspx) <br/> |
||[NewFromFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) <br/> |
||[NewFromFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) <br/> |
||[NewFromFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) <br/> |
||[NewFromFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) <br/> |
||[Open](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Open.aspx) <br/> |
||[Open](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Open.aspx) <br/> |
|[XmlFormOpenMode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormOpenMode.aspx) <br/> |**XmlFormOpenMode.Default** <br/> |
||**XmlFormOpenMode.FailOnVersionMismatch** <br/> |
||**XmlFormOpenMode.FailOnVersionOlder** <br/> |
||**XmlFormOpenMode.IgnoreDataConnectionsFailure** <br/> |
||**XmlFormOpenMode.PromptIfSigned** <br/> |
||**XmlFormOpenMode.ReadOnly** <br/> |
||**XmlFormOpenMode.TransformEvenIfSigned** <br/> |
||**XmlFormOpenMode.UseExistingVersion** <br/> |
||**XmlFormOpenMode.UseFileConverter** <br/> |
|[XmlValidatingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) <br/> |[ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) <br/> |
   

