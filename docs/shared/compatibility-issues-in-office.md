---
title: Office の互換性に関する問題
manager: lindalu
ms.date: 12/03/2019
ms.audience: Developer
ms.assetid: dd279238-ae75-4ad9-b9e5-364924090485
description: Office 製品で起きる可能性のある互換性の問題に関するテレメトリ ログに表示される問題について、詳細情報を取得します。
ms.localizationpriority: high
ms.openlocfilehash: 1398db2e0dcbde354c713c08f6875c8a9910dea0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586692"
---
# <a name="compatibility-issues-in-office"></a>Office の互換性に関する問題

Office 製品で起きる可能性のある互換性の問題に関するテレメトリ ログに表示される問題について、詳細情報を取得します。
  
次の表では、テレメトリ ログに表示される問題についての情報を一覧表示します。テレメトリ ログの詳細については、「[テレメトリ ログを使用した Office ファイルおよびカスタム ソリューションのトラブルシューティング](troubleshooting-office-files-and-custom-solutions-with-the-telemetry-log.md)」を参照してください。
  
Office 2013 から変更または削除されている機能の詳細については、「[Windows Office 2016 における変更](https://docs.microsoft.com/DeployOffice/office2016/changes-in-office-2016-for-windows-desktop)」を参照してください。
  
## <a name="controls"></a>Controls
<a name="OEV_CompatIssues_Controls"> </a>

これらのメッセージは、Office またはコンピューターのオペレーティング システムでサポートされていないコントロールがファイルに含まれていると、表示される場合があります。
  
**表 1.コントロールに関するテレメトリ ログに表示される問題**

|**イベント ID**|**導入されたバージョン**|**影響を受けるアプリケーション**|**追加情報**|**タイトル**|**説明**|
|:-----|:-----|:-----|:-----|:-----|:-----|
|10000  <br/> |Office 2013  <br/> |全 Office 2013  <br/> ||警告: Visual Basic 6.0 のコントロール  <br/> |このファイルで使われている Visual Basic 6.0 コントロールは、64 ビット バージョンの Office や、ARM プロセッサが使われているデバイス で実行中の 32 ビット バージョンの Office では機能 しません。それらの環境の Office アプリケーションで使えるようにす るには、サポートされているコントロールに置き換えてください。  <br/> |
|10001  <br/> |Office 2013  <br/> |すべての Office 2013  <br/> |[リンク](https://docs.microsoft.com/previous-versions/visualstudio/visual-basic-6/visual-basic-6-support-policy) <br/> |コントロール: Visual Basic 6.0 コントロール (64 ビット OS)  <br/> |このファイルで使われている Visual Basic 6.0 コントロールは、64 ビット バージョンの Office では機能しません。Visual Basic 6.0 ラ ンタイム ファイルは 32 ビットであり、32 ビット OS または WOW エミュレーショ ン環境でのみサポートされます。  <br/> |
|10002  <br/> |Office 2013  <br/> |すべての Office 2013  <br/> |[リンク](https://docs.microsoft.com/previous-versions/visualstudio/visual-basic-6/visual-basic-6-support-policy) <br/> |コントロール: Visual Basic 6.0 コントロール (ARM プロセッサ搭 載デバイス)  <br/> |このファイルで使われている Visual Basic 6.0 コントロールは、ARM プロセッサを使用するデバ イスでは機能しません。  <br/> |
|10003  <br/> |Office 2013  <br/> |すべての Office 2013  <br/> |[リンク](https://docs.microsoft.com/previous-versions/office/office-2010/cc179181(v=office.14)) <br/> |コントロール: Microsoft カレンダー コントロール  <br/> |The file uses the Microsoft Calendar control (Mscal.ocx), a feature of previous versions of Access that is not available in Office 2013. The control will not work because it is not installed on the host computer. Use other date picker controls as an alternative, like the **Date Picker Content Control** (in Word 2013) or the Windows **DatePicker** control (in the Windows Common Controls).  <br/> 詳細については、「[Access 2010 アプリケーションのカレンダー コントロールを置き換える](https://docs.microsoft.com/previous-versions/office/developer/office-2010/gg251104(v=office.14))」を参照してください。  <br/> |
|10004  <br/> |Office 2013  <br/> |すべての Office 2013  <br/> |[リンク](https://social.msdn.microsoft.com/Forums/6497460b-db0b-4ae1-8b15-3ab14f08ab68/vba-spreadsheet-control-doesnt-work-on-excel-2013?forum=officegeneral) <br/> |Office Web コンポーネント  <br/> |このファイルは Office Web コンポーネント コントロールを使いますが、Office Web コンポーネントがこのコンピュー ターにインストールされておらず、Office 2013に含まれていないため、コントロー ルは機能しません。このコントロールを使うには、Office Web コンポーネントを個別にインストー ルする必要があります。  <br/> 詳細については、「[Office Web コンポーネント (OWC) のプログラミングに役立つ各種情報とサンプル](https://support.microsoft.com/help/319793/how-to-find-office-web-components-owc-programming-documentation-and-sa)」を参照してください。 <br/> |
|10005  <br/> |Office 2013  <br/> |すべての Office 2013  <br/> |[リンク](https://support.office.com/article/embedded-object-and-activex-control-policy-settings-error-acb9e88e-88fa-4440-96af-50490a301fc4) <br/> |コントロール: 未登録の ActiveX コントロール  <br/> |このファイルは、ホスト コンピューターに登録されていない ActiveX コントロールを使用します。このコントロールを使用するには、ホスト コンピューターに登録してください。  <br/> |
   
## <a name="removed-and-deprecated-members-in-the-object-model"></a>削除されて使用されなくなったオブジェクト モデルのメンバー
<a name="OEV_CompatIssues_Removed"> </a>

これらのメッセージは、アドインまたはマクロが有効なドキュメントのコードで、推奨されないオブジェクト、メンバー、コレクション、列挙体、または定数が使用されていると、表示される場合があります。 
  
**表 2.削除されて使用されなくなったメンバーに関するテレメトリ ログに表示される問題**

|**イベント ID**|**導入されたバージョン**|**影響を受けるアプリケーション**|**追加情報**|**タイトル**|**説明**|
|:-----|:-----|:-----|:-----|:-----|:-----|
|10103  <br/> |Office 2013  <br/> |Word 2013, Outlook 2013  <br/> |[リンク](https://docs.microsoft.com/office/troubleshoot/word/custom-xml-elements-not-supported) <br/> |オブジェクト モデル削除済み: カスタム XML 機能  <br/> | カスタム XML 機能は Word から削除されています。次のメソッドおよびプロパティは推奨されません。アクセスすると実行時エラーが返されます。<br/><br/>- **XMLNodes.Add** メソッド  <br/>- **Document.XMLHideNamespaces** プロパティ  <br/>- **Document.XMLSaveDataOnly** プロパティ  <br/>- **Document.XMLSchemaViolations** プロパティ  <br/>- **XMLSchemaViolations** オブジェクトおよびそのすべてのメンバー  <br/>- **XMLSchemaViolation** オブジェクトおよびそのすべてのメンバー  <br/>- **Application.TaskPanes**、**WdTaskPanes** 列挙体の **wdTaskPaneXMLStructure** 定数 (5) が指定されている場合  <br/>- **Options.PrintXMLTag** プロパティ  <br/>- **View.ShowXMLMarkup** プロパティ  <br/>- **XMLChildNodeSuggestions** コレクションおよびそのすべてのメンバー  <br/>- **XMLChildNodeSuggestion** オブジェクトおよびそのすべてのメンバー  <br/>- **Selection.XMLParentNode** プロパティ  <br/>- **Range.XMLParentNode** プロパティ  <br/> |
|10113  <br/> |Office 2013  <br/> |Word 2013, Outlook 2013  <br/> ||OM 削除済み: スマート タグ機能  <br/> | スマート タグ機能は Word から削除されています。次のオブジェクト、メソッド、およびプロパティは推奨されません。アクセスすると実行時エラーが返されます。<br/>- **SmartTag** オブジェクトおよびメンバー  <br/>- **SmartTags** コレクションおよびメンバー  <br/>- **SmartTagAction** オブジェクトおよびメンバー  <br/>- **SmartTagActions** コレクションおよびメンバー  <br/>- **SmartTagType** オブジェクトおよびメンバー  <br/>- **SmartTagTypes** コレクションおよびメンバー  <br/>- **XMLNode.SmartTag** プロパティ  <br/><br/>  次のメソッドは表示されず、アクセスすると通知なしに失敗します。  <br/>- **Document.CheckNewSmartTags** メソッド  <br/>- **Document.RecheckSmartTags** メソッド  <br/>- **Document.RemoveSmartTags** メソッド  <br/><br/>次のプロパティは表示されず、アクセスすると常に FALSE が返されます。  <br/>- **Document.EmbedSmartTags** プロパティ  <br/>- **Document.SmartTagsAsXMLProps** プロパティ  <br/>- **Options.LabelSmartTags** プロパティ  <br/>- **Options.DisplaySmartTagButtons** プロパティ  <br/>- **EmailOptions.EmbedSmartTag** プロパティ  <br/><br/>次のプロパティは表示されず、アクセスすると常に true が返されます。  <br/>- **View.DisplaySmartTags** プロパティ<br/><br/>  次のプロパティは表示されず、アクセスすると常に空のコレクションが返されます。  <br/>- **Application.SmartTagTypes** プロパティ  <br/>- **Document.SmartTags** プロパティ  <br/>- **Range.SmartTags** プロパティ  <br/>- **Selection.SmartTags** プロパティ  <br/> |
|10115  <br/> |Office 2013  <br/> |Word 2013, Outlook 2013  <br/> ||オブジェクト モデル削除済み: 自動要約機能  <br/> | 自動要約機能は Word から削除されています。次のメソッドおよびプロパティは推奨されません。アクセスすると実行時エラーが返されます。<br/>- **Document.AutoSummarize** メソッド  <br/>- **Document.ShowSummary** プロパティ  <br/>- **Document.SummaryViewMode** プロパティ  <br/>- **Document.SummaryLength** プロパティ  <br/> |
|10116  <br/> |Office 2013  <br/> |Word 2013、Outlook 2013  <br/> ||オブジェクト モデル削除済み: バーコード機能  <br/> | 封筒のバーコード機能は Word から削除されています。次のプロパティは非公開になっていて、アクセスすると常に FALSE が返されます。<br/>- **Envelope.DefaultPrintBarCode** プロパティ  <br/>- **MailingLabel.DefaultPrintBarCode** プロパティ  <br/> |
|10117  <br/> |Office 2013  <br/> |Word 2013, Outlook 2013  <br/> ||オブジェクト モデル削除済み: Window.DocumentMapPercentWidth プロパティ  <br/> |**Window.DocumentMapPercentWidth** プロパティは Word では推奨されません。このプロパティにアクセスすると実行時エラーが発生します。<br/> |
|10122  <br/> |Office 2013  <br/> |Word 2013, Outlook 2013  <br/> ||OM 削除済み: Application.FileSearch  <br/> |**Application.FileSearch** は Office 2007 で削除されました。このプロパティにアクセスすると、エラーが返されます。この問題を解決するには、 [FileSystemObject](https://docs.microsoft.com/office/vba/Language/Reference/User-Interface-Help/filesystemobject-object) を使用してディレクトリを再帰的に検索し、目的のファイルを探してください。  <br/> |
|10145  <br/> |Office 2013  <br/> |Excel 2013  <br/> ||OM 削除済み: Application.FileSearch  <br/> |**Application.FileSearch** プロパティは Office 2007 で削除されました。このプロパティにアクセスすると、エラーが返されます。この問題を解決するには、 [FileSystemObject](https://docs.microsoft.com/office/vba/Language/Reference/User-Interface-Help/filesystemobject-object) を使用してディレクトリを再帰的に検索し、目的のファイルを探してください。  <br/> |
|10154  <br/> |Office 2013  <br/> |Excel 2013  <br/> ||OM 削除済み: スマート タグ機能  <br/> | スマート タグ機能は Excel から削除されています。次のプロパティは表示されず、アクセスすると常に FALSE が返されます。  <br/>- **Application.SmartTagRecognizers** プロパティ  <br/><br/>次のオブジェクト、メソッド、およびプロパティは表示されず、アクセスすると実行時エラーが返されます。  <br/>- **SmartTag** オブジェクトおよびメンバー  <br/>- **SmartTags** コレクションおよびメンバー  <br/>- **SmartTagAction** オブジェクトおよびメンバー  <br/>- **SmartTagActions** コレクションおよびメンバー  <br/>- **SmartTagOptions** コレクションおよびメンバー  <br/>- **SmartTagRecognizer** オブジェクトおよびメンバー  <br/>- **SmartTagRecognizers** コレクションおよびメンバー  <br/><br/>  次のメソッドは表示されず、アクセスすると通知なしに失敗します。  <br/>- **Workbook.RecheckSmartTags** メソッド  <br/><br/>次のプロパティは表示されず、アクセスすると常に空のコレクションが返されます。  <br/>- **Workbook.SmartTagOptions** プロパティ  <br/>- **Worksheet.SmartTags** プロパティ  <br/>- **Range.SmartTags** プロパティ  <br/>- **IRange.SmartTags** プロパティ  <br/>- **DialogSheet.SmartTags** プロパティ  <br/>- **IDialogSheet.SmartTags** プロパティ  <br/> |
|10155  <br/> |Office 2013  <br/> |すべての Office 2013  <br/> ||オブジェクト モデル削除済み: ToolbarButton.Edit メソッド  <br/> |CommandBar Button Editor は削除されました。このメソッドを呼び出すと、通知なしに失敗します。レガシ CommandBar ボタンにカスタム イメージを適用するには、[CommandBarButton.PasteFace](https://docs.microsoft.com/office/vba/api/Office.CommandBarButton.PasteFace) メソッドまたは [CommandBarButton.Picture](https://docs.microsoft.com/office/vba/api/Office.CommandBarButton.Picture) プロパティと [CommandBarButton.Mask](https://docs.microsoft.com/office/vba/api/Office.CommandBarButton.Mask) プロパティを使用します。  <br/> |
|10159  <br/> |Office 2016  <br/> |Word  <br/> ||使用されなくなったオブジェクト モデル：SkyDriveSignInOption  <br/> |SkyDriveSignInOption は使用されなくなりました。代わりに、CloudSignInOption を使用してください。  <br/> |
   
## <a name="behavior-changes-in-the-object-model"></a>動作が変更されたオブジェクト モデル
<a name="OEV_CompatIssues_Changed"> </a>

これらのメッセージは、アドインまたはマクロが有効なドキュメントのコードで、前のバージョンの Office と動作が異なるオブジェクト、メンバー、コレクション、列挙体、または定数が使用されていると、表示される場合があります。
  
**表 3. 動作変更に関するテレメトリ ログに表示される問題**

|**イベント ID**|**導入されたバージョン**|**影響を受けるアプリケーション**|**追加情報**|**タイトル**|**説明**|
|:-----|:-----|:-----|:-----|:-----|:-----|
|10156  <br/> |Office 2016  <br/> |Word  <br/> ||オブジェクト モデルの動作変更:保存イベントの使用が検出された  <br/> |互換性チェックで、リアルタイム共同編集中に、望ましくない体験を引き起こす可能性がある保存イベントが使用されていることが検出されました。そのような状況で保存頻度が高くなると、リアルタイム共同編集セッション中にソリューションが意図したとおりに動作しないことがあります。保存を頻繁に行うときは、ソリューションを絞るよう調整することをお勧めします。あるいは、グループ ポリシーを使用してリアルタイム共同編集を無効にします。  <br/> |
|10160  <br/> |Office 2016  <br/> |Word、Excel、PowerPoint  <br/> ||オブジェクト モデルの動作変更:Application.DisplayDocumentInformationPanel  <br/> |InfoPath 製品廃止に伴い、ドキュメント情報パネルは廃止されました。このプロパティのクエリは常に false を返します。このプロパティの設定は、アプリケーションによって異なります。True に設定すると、Word および PowerPoint でプロパティ パネルを表示します。Excel では何もしません。False に設定すると、すべてのアプリで何もしません。  <br/> |
|10161  <br/> |Office 2016  <br/> |Word  <br/> ||オブジェクト モデルの動作変更:ContentControl.DropdownListEntries  <br/> |InfoPath 製品廃止に伴い、ドキュメント情報パネルは廃止されました。SharePoint のルックアップ プロパティに対して、この API の動作はサポートされなくなりました。その他の種類のリスト エントリでは、期待どおりに機能します。  <br/> |
|10157  <br/> |Office 2016  <br/> |PowerPoint  <br/> ||オブジェクト モデルの動作変更:Presentation.InMergeMode プロパティ  <br/> |共同編集が新しい競合するソリューション ウィンドウに置き換わったときに、古い結合モードがドキュメント ウィンドウに現れます。この状況でアクセスすると、Presentation.InMergeMode プロパティから False が返されます。  <br/> |
|10106  <br/> |Office 2013  <br/> |Excel 2013  <br/> ||オブジェクト モデル動作変更: Application.FormulaBarHeight プロパティ  <br/> |[Application.FormulaBarHeight プロパティ (Excel)](https://docs.microsoft.com/office/vba/api/Excel.Application.FormulaBarHeight) プロパティは変更されています。このプロパティにアクセスすると、Excel のアクティブ ウィンドウに関連付けられた数式バーの高さの取得と設定を行うことができます。Excel の別のウィンドウの数式バーの高さを変更するには、対象のウィンドウをアクティブにしてから **Application.FormulaBarHeight** プロパティを設定します。  <br/> |
|10107  <br/> |Office 2013  <br/> |Excel 2013  <br/> ||オブジェクト モデル動作変更: Workbook.Protect メソッド  <br/> |Excel のウィンドウ構造 (高さ、幅、最小化または最大化された状態) は保護されません。[Workbook.Protect メソッド (Excel)](https://docs.microsoft.com/office/vba/api/Excel.Workbook.Protect) メソッドを呼び出しても、Windows パラメーターの値にかかわらず、ワークブックのウィンドウ構造は保護されません。<br/> |
|10140  <br/> |Office 2013  <br/> |Word 2013, Outlook 2013  <br/> ||オブジェクト モデル動作変更: Table.AllowPageBreaks  <br/> |**Table.AllowPageBreaks** プロパティは非推奨で、常に TRUE が返されます。同じ動作を実現するには、 [ParagraphFormat.KeepTogether プロパティ (Word)(機械翻訳)](https://docs.microsoft.com/office/vba/api/Word.ParagraphFormat.KeepTogether) および [ParagraphFormat.KeepWithNext プロパティ (Word)(機械翻訳)](https://docs.microsoft.com/office/vba/api/Word.ParagraphFormat.KeepWithNext) の各プロパティを使用します。  <br/> |
   
## <a name="hidden-members-in-the-object-model"></a>推奨されないオブジェクト モデルのメンバー
<a name="OEV_CompatIssues_Hidden"> </a>

これらのメッセージは、アドインまたはマクロが有効なドキュメントのコードで、推奨されないオブジェクト、メンバー、コレクション、列挙体、または定数が使用されていると、表示される場合があります。
  
**表 4. 非表示メンバーに関するテレメトリ ログに表示される問題**

|**イベント ID**|**導入されたバージョン**|**影響を受けるアプリケーション**|**追加情報**|**タイトル**|**説明**|
|:-----|:-----|:-----|:-----|:-----|:-----|
|10158  <br/> |Office 2016  <br/> |Excel  <br/> ||非表示のオブジェクト モデル:Presentation.WorksheetFunction.Forecast (すべて) メソッド  <br/> |WorksheetFunction.Forecast メソッドは非表示です。呼び出されたメソッドは、Excel 2013 におけるのと同様に動作します。下位互換性を保つためオブジェクト モデルの一部として残っていますが、新しいアプリケーションでは WorksheetFunction.Forecast_Linear を使用する必要があります。  <br/> |
|10109  <br/> |Office 2013  <br/> |Word 2013, Outlook 2013  <br/> ||非推奨オブジェクト モデル: Document.UpdateSummaryProperties メソッド  <br/> |自動要約機能は Word から削除されました。**Document.UpdateSummaryProperties** メソッドを呼び出すと、実行時エラーが返されます。<br/> |
|10110  <br/> |Office 2013  <br/> |Word 2013, Outlook 2013  <br/> ||非推奨オブジェクト モデル: Comment.Delete メソッド  <br/> |Word ではコメントに直接返信できます。 **Comment.Delete** メソッドを呼び出すと、以前のバージョンの Office の動作と同じように、コメントを削除してドキュメントに全返信を残します。コメントの全スレッドを削除するには、 **Comment.DeleteRecursively** メソッドを使用します。コメントに返信するには、 **Comment.Replies.Add** メソッドを使用します。  <br/> |
|10111  <br/> |Office 2013  <br/> |Word 2013, Outlook 2013  <br/> ||非推奨オブジェクト モデル: Comment.Author プロパティ  <br/> |現在、Word のコメントは作成者と関連付けられています。 **Comment.Author** プロパティにアクセスすると、以前のバージョンの Office と同じように動作します。コメント投稿者の名前にアクセスするには、コメントに関連付けられている **Contact** オブジェクトの Name プロパティを使用します。  <br/> |
|10112  <br/> |Office 2013  <br/> |Word 2013, Outlook 2013  <br/> ||非推奨オブジェクト モデル: Comment.Initial プロパティ  <br/> |既定では、Word のコメントにコメント投稿者のイニシャルは表示されません。 **Comment.Initial** プロパティにアクセスすると、以前のバージョンの Office と同じように動作します。ただし、印刷されたドキュメントでは引き続きコメントにイニシャルが表示されます。  <br/> |
|10114  <br/> |Office 2013  <br/> |Word 2013, Outlook 2013  <br/> ||非推奨オブジェクト モデル: Comment.ShowTip プロパティ  <br/> |Word のコメントに関連付けられたポップ ヒントは既定で表示されます。 **Comment.ShowTip** プロパティにアクセスすると、常に FALSE が返されます。  <br/> |
|10118  <br/> |Office 2013  <br/> |Word 2013、Outlook 2013  <br/> ||非推奨オブジェクト モデル: Options.BackgroundOpen プロパティ  <br/> |大きな Web ドキュメントを Word のバックグラウンドで開くことはできません。[Options.BackgroundOpen プロパティ (Word)(機械翻訳)](https://docs.microsoft.com/previous-versions/office/ff840248(v=office.15)) プロパティにアクセスすると、常に FALSE が返され、別の値に設定できません。<br/> |
|10119  <br/> |Office 2013  <br/> |Word 2013, Outlook 2013  <br/> ||非推奨オブジェクト モデル: Document.ApplyQuickStyleSet メソッド  <br/> |**Document.ApplyQuickStyleSet** メソッドは Word では推奨されません。このメソッドを呼び出すと、引き続き Office 2007 での動作と同じように機能し、ドキュメントのスタイル セットを変更します。Office 2010 以降の新機能を使用するには、 [Document.ApplyQuickStyleSet2 メソッド (Word)(機械翻訳)](https://docs.microsoft.com/office/vba/api/Word.Document.ApplyQuickStyleSet2) メソッドに置き換えます。  <br/> |
|10120  <br/> |Office 2013  <br/> |Word 2013, Outlook 2013  <br/> ||非推奨オブジェクト モデル: Document.SaveAs メソッド  <br/> |「名前を付けて保存」機能は、以前のバージョンの Word と同じように動作します。 **Document.SaveAs** メソッドを呼び出すと、Office 2007 の場合と同じように動作します。 また、Document オブジェクトには **SaveAs2** メソッドが追加されています。このメソッドには、Office 2010 で導入されたプロパティが含まれています。 Office 2010 以降の新機能を使用する場合は、**Document.SaveAs** メソッドを [Document.SaveAs2 メソッド (Word)](https://docs.microsoft.com/office/vba/api/Word.SaveAs2) に置き換えてください。  <br/> |
|10121  <br/> |Office 2013  <br/> |Word 2013, Outlook 2013  <br/> ||非推奨オブジェクト モデル: アシスタント機能およびアンサー ウィザード機能  <br/> | Word では、アシスタント機能とアンサーウィザード機能は非推奨になりました。  <br/><br/>以下のプロパティは下位互換性を保つためオブジェクト モデルの一部として残っていますが、新しい Office ソリューションでは使用しないでください。  <br/>- **Application.Assistant** プロパティ  <br/>- **Application.AnswerWizard** プロパティ  <br/><br/>以下のプロパティは非推奨で、これらのプロパティにアクセスすると実行時エラーが返されます。<br/>- **Global.Assistant** プロパティ  <br/>- **Global.AnswerWizard** プロパティ  <br/> |
|10123  <br/> |Office 2013  <br/> |Word 2013, Outlook 2013  <br/> ||非推奨オブジェクト モデル: Options.WPHelp  <br/> |**Options.WPHelp** プロパティは推奨されません。  <br/> |
|10124  <br/> |Office 2013  <br/> |Word 2013, Outlook 2013  <br/> ||非推奨オブジェクト モデル: Options.SetWPHelpOptions  <br/> |**Options.SetWPHelpOptions** プロパティは推奨されません。このプロパティにアクセスすると、エラーが返されます。  <br/> |
|10125  <br/> |Office 2013  <br/> |Word 2013, Outlook 2013  <br/> ||非推奨オブジェクト モデル: Options.WPDocNavKeys  <br/> |**Options.WPDocNavKeys** プロパティは推奨されません。このプロパティにアクセスすると、常に FALSE が返されます。  <br/> |
|10126  <br/> |Office 2013  <br/> |Word 2013, Outlook 2013  <br/> ||非推奨オブジェクト モデル: Options.BlueScreen  <br/> |**Options.BlueScreen** プロパティは推奨されません。このプロパティにアクセスすると、常に FALSE が返されます。  <br/> |
|10127  <br/> |Office 2013  <br/> |Word 2013, Outlook 2013  <br/> ||非推奨オブジェクト モデル: Options.AllowFastSave  <br/> |**Options.AllowFastSave** は推奨されません。このプロパティにアクセスすると、常に FALSE が返されます。  <br/> |
|10128  <br/> |Office 2013  <br/> |Word 2013, Outlook 2013  <br/> ||非推奨オブジェクト モデル: Application.DisplayStatusBar  <br/> |**Application.DisplayStatusBar** プロパティは推奨されません。代わりに **Application.CommandBars("Status Bar")** Visible を使用してください。  <br/> |
|10129  <br/> |Office 2013  <br/> |Word 2013Outlook 2013  <br/> ||非推奨オブジェクト モデル: Document.HTMLProject  <br/> |**Document.HTMLProject** は推奨されません。このプロパティにアクセスすると、エラーが返されます。  <br/> |
|10130  <br/> |Office 2013  <br/> |Word 2013, Outlook 2013  <br/> ||非推奨オブジェクト モデル: Document.Versions  <br/> |版の管理機能は削除されているため、 **Document.Versions** プロパティは推奨されません。このプロパティにアクセスすると、エラーが返されます。  <br/> |
|10131  <br/> |Office 2013  <br/> |Word 2013, Outlook 2013  <br/> ||非推奨オブジェクト モデル: Document.Route  <br/> |回覧機能は削除されているため、 **Document.Route** メソッドは推奨されません。このメソッドにアクセスすると、エラーが返されます。  <br/> |
|10132  <br/> |Office 2013  <br/> |Word 2013, Outlook 2013  <br/> ||非推奨オブジェクト モデル: Document.HasRoutingSlip  <br/> |回覧機能は削除されているため、 **Document.HasRoutingSlip** プロパティは推奨されません。このプロパティにアクセスすると、エラーが返されます。  <br/> |
|10133  <br/> |Office 2013  <br/> |Word 2013, Outlook 2013  <br/> ||非推奨オブジェクト モデル: Document.Routed  <br/> |回覧機能は削除されているため、 **Document.Routed** プロパティは推奨されません。このプロパティにアクセスすると、エラーが返されます。  <br/> |
|10134  <br/> |Office 2013  <br/> |Word 2013、Outlook 2013  <br/> ||非推奨オブジェクト モデル: Document.RoutingSlip  <br/> |回覧機能は削除されているため、 **Document.RoutingSlip** プロパティは推奨されません。このプロパティにアクセスすると、エラーが返されます。  <br/> |
|10135  <br/> |Office 2013  <br/> |Word 2013, Outlook 2013  <br/> ||非推奨オブジェクト モデル: Diagram OM  <br/> | **Diagram** オブジェクトおよび **Diagram** オブジェクトに関連付けられているプロパティやメソッドは非公開になっています。次のメンバーにアクセスすると、エラーが生成されます。<br/>- **Shapes.AddDiagram** <br/>- **Shape.Diagram** <br/>- **Shape.DiagramNode** <br/>- **Shape.HasDiagram** <br/>- **ShapeHasDiagramNode** <br/>- **ShapeRange.DiagramNode** <br/>- **ShapeRange.HasDiagram** <br/>- **ShapeRange.HasDiagramNode** <br/> |
|10136  <br/> |Office 2013  <br/> |Word 2013, Outlook 2013  <br/> ||非推奨オブジェクト モデル: ShapeRange.Activate  <br/> | Word Word 図オブジェクトは非推奨のため、画像を Word 図オブジェクトに変換するメソッドも非推奨になりました。該当するメソッドは次のとおりです。  <br/>- **InlineShape.Activate** <br/>- **Shape.Activate** <br/>- **ShapeRange.Activate** <br/><br/>  これらのメソッドを使用すると、エラーが生成されます。  <br/> |
|10137  <br/> |Office 2013  <br/> |Word 2013, Outlook 2013  <br/> ||非推奨オブジェクト モデル: Shape.Activate  <br/> | Word Word 図オブジェクトは非推奨のため、画像を Word 図オブジェクトに変換するメソッドも非推奨になりました。該当するメソッドは次のとおりです。  <br/>- **InlineShape.Activate** <br/>- **Shape.Activate** <br/>- **ShapeRange.Activate** <br/><br/>これらのメソッドを使用すると、エラーが生成されます。  <br/> |
|10138  <br/> |Office 2013  <br/> |Word 2013, Outlook 2013  <br/> ||非推奨オブジェクト モデル: InlineShape.Activate  <br/> | Word Word 図オブジェクトは非推奨のため、画像を Word 図オブジェクトに変換するメソッドも非推奨になりました。該当するメソッドは次のとおりです。  <br/>- **InlineShape.Activate** <br/>- **Shape.Activate** <br/>- **ShapeRange.Activate** <br/><br/>これらのメソッドを使用すると、エラーが生成されます。  <br/> |
|10139  <br/> |Office 2013  <br/> |Word 2013  <br/> ||OM 非推奨: Shapes.AddChart  <br/> |**Shapes.AddChart** メソッドは推奨されません。下位互換性を保つためオブジェクト モデルの一部として残っていますが、新しいアプリケーションでは使用しないでください。代わりに **Shapes.AddChart2** メソッドを使用してください。  <br/> <br/>**注**: **Shapes.AddChart2** メソッドは、新しいグラフに既定のタイトルを適用します。 ファイルにグラフを追加した後でグラフのタイトルを変更する場合は、**Chart.ChartTitle** プロパティを使用するか、手動でタイトルを編集します。           |
|10141  <br/> |Office 2013  <br/> |Word 2013, Outlook 2013  <br/> ||非推奨オブジェクト モデル: Application.ShowWindowsInTaskbar  <br/> |**Application.ShowWindowinTaskbar** プロパティは推奨されません。このプロパティにアクセスすると、常に true が返されます。  <br/> |
|10142  <br/> |Office 2013  <br/> |Word 2013, Outlook 2013  <br/> ||非推奨オブジェクト モデル: HangulHanjaConversionDictionaries.BuiltinDictionary  <br/> |**HangulHanjaConversionDictionaries.BuiltinDictionary** プロパティは推奨されません。このプロパティにアクセスすると、NULL が返されます。  <br/> |
|10143  <br/> |Office 2013  <br/> |Word 2013, Outlook 2013  <br/> ||非推奨オブジェクト モデル: Template.AutoTextEntries  <br/> |現在、定型句は構成要素の一部です。構成要素にアクセスするには、[Template.BuildingBlockEntries プロパティ (Word)(機械翻訳)](https://docs.microsoft.com/office/vba/api/Word.Template.BuildingBlockEntries) または [Template.BuildingBlockTypes プロパティ (Word)(機械翻訳)](https://docs.microsoft.com/office/vba/api/Word.Template.BuildingBlockTypes) の各プロパティを使用します。  <br/> 既定では、定型句は normal.dotm に保存されます。  <br/> |
|10144  <br/> |Office 2013  <br/> |Word 2013, Outlook 2013  <br/> ||OM 非推奨: View.RevisionsMode  <br/> |**View.RevisionsMode** プロパティは推奨されません。代わりに [View.MarkupMode プロパティ (Word)(機械翻訳)](https://docs.microsoft.com/office/vba/api/Word.View.MarkupMode) プロパティを使用してください。  <br/> |
|10146  <br/> |Office 2013  <br/> |Excel 2013  <br/> ||OM 非推奨: ISlicerCache.ClearManualFilter  <br/> |ISlicerCache オブジェクトのメソッド **ClearManualFilter** は非表示とマークされていました。下位互換性を保つためオブジェクト モデルの一部として残っていますが、新しいアプリケーションでは使用しないでください。  <br/> |
|10147  <br/> |Office 2013  <br/> |Excel 2013  <br/> ||OM 非推奨: _Application.ShowWindowsInTaskbar  <br/> |プロパティ **\_Application.ShowWindowsInTaskbar** は推奨されません。下位互換性を保つためオブジェクト モデルの一部として残っていますが、新しいアプリケーションでは使用しないでください。<br/> |
|10148  <br/> |Office 2013  <br/> |Excel 2013  <br/> ||OM 非推奨: _Application.SaveISO8601Dates  <br/> |プロパティ **\_Application.SaveISO8601Dates** は推奨されません。下位互換性を保つためオブジェクト モデルの一部として残っていますが、新しいアプリケーションでは使用しないでください。<br/> |
|10149  <br/> |Office 2013  <br/> |Excel 2013  <br/> ||OM 非推奨: SlicerCache.ClearManualFilter  <br/> |SlicerCache. オブジェクトのメソッド **ClearManualFilter** は推奨されません。下位互換性を保つためオブジェクト モデルの一部として残っていますが、新しいアプリケーションでは使用しないでください。  <br/> |
|10150  <br/> |Office 2013  <br/> |Excel 2013  <br/> ||OM 非推奨: _Application.Assistant  <br/> |プロパティ **\_Application.Assistant** は推奨されません。下位互換性を保つためオブジェクト モデルの一部として残っていますが、新しいアプリケーションでは使用しないでください。<br/> |
|10151  <br/> |Office 2013  <br/> |Excel 2013  <br/> ||OM 非推奨: _Application.AnswerWizard  <br/> |プロパティ **\_Application.Assistant** は推奨されません。このプロパティにアクセスすると実行時エラーが返されます。<br/> |
|10152  <br/> |Office 2013  <br/> |Excel 2013  <br/> ||OM 非推奨: _Global.Assistant  <br/> |プロパティ **\_Global.Assistant** は推奨されません。下位互換性を保つためオブジェクト モデルの一部として残っていますが、新しいアプリケーションでは使用しないでください。<br/> |
|10153  <br/> |Office 2013  <br/> |Excel 2013  <br/> ||OM 非推奨: Shapes.AddChart  <br/> |**Shapes.AddChart** メソッドは推奨されません。下位互換性を保つためオブジェクト モデルの一部として残っていますが、新しいアプリケーションでは使用しないでください。代わりに **Shapes.AddChart2** メソッドを使用してください。  <br/> <br/>**注**: **Shapes.AddChart2** メソッドは、新しいグラフに既定のタイトルを適用します。 ファイルにグラフを追加した後でグラフのタイトルを変更する場合は、**Chart.ChartTitle** プロパティを使用するか、手動でタイトルを編集します。           |
   
## <a name="see-also"></a>関連項目

- [Office での互換性とテレメトリ](https://docs.microsoft.com/previous-versions/office/office-2013-resource-kit/ff394407(v=office.15)) 
- [Office デベロッパー センター](https://developer.microsoft.com/office)
- [テレメトリ ログを使用した Office ファイルおよびカスタム ソリューションのトラブルシューティング](troubleshooting-office-files-and-custom-solutions-with-the-telemetry-log.md)
- [Office アプリケーション互換性フォーラム](https://social.technet.microsoft.com/Forums/officesetupdeploy/threads)
    

