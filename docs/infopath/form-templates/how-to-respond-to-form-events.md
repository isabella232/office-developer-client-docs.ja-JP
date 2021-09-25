---
title: フォーム イベントに応答する
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- イベントの順序 [infopath 207],イベント [InfoPath 2007],応答,イベント [InfoPath 2007],順序,InfoPath 2007,イベントに応答する,EventArgs クラス [InfoPath 2007]
ms.localizationpriority: medium
ms.assetid: 754db64b-179f-4385-8dd9-c20c9407b186
description: ユーザーがフォームに入力する際に発生する各種イベントに応答するコードを書くことができます。InfoPath 内でイベントの作業を実行するには、デザイン モードのフォーム テンプレートの作業中にイベント ハンドラーを追加します。
ms.openlocfilehash: fdc099e65365eecfc114642760734e7a48c3c5ca
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592852"
---
# <a name="respond-to-form-events"></a>フォーム イベントに応答する

ユーザーがフォームに入力する際に発生する各種イベントに応答するコードを書くことができます。InfoPath 内でイベントの作業を実行するには、デザイン モードのフォーム テンプレートの作業中にイベント ハンドラーを追加します。
  
InfoPath イベント ハンドラーは常にデザイン モードで作成する必要があります。これは、InfoPath ではイベントを **InternalStartup** メソッドにシンクするための正しい宣言が自動的に追加され、イベント ハンドラーのコード スケルトンがフォームのコード ファイル (FormCode.cs または FormCode.vb) に挿入されるためです。イベント ハンドラーを作成した後、フォームのコード ファイルの宣言は変更しないでください。 
  
InfoPath イベント ハンドラーの作成について詳しくは、「[イベント ハンドラーを追加する方法](how-to-add-an-event-handler.md)」を参照してください。
  
## <a name="overview-of-the-event-classes"></a>イベント クラスの概要

[Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) 名前空間によって提供される InfoPath モデルでは、12 個のイベントを実装する 3 つのクラスを実装します。イベントはフォーム テンプレート ビジネス ロジックにより発生させ、処理することができます。次の表に、各 InfoPath イベント オブジェクト、関連付けられたイベント、およびその機能を示します。 
  
|**名前**|**イベント**|**説明**|
|:-----|:-----|:-----|
|[ButtonEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.aspx) <br/> |[Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) <br/> |**ButtonEvent** クラスは、フォーム上の [ **ボタン**] コントロールがクリックされると発生する **Clicked** イベントを実装します。  <br/> |
|[FormEvents](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.aspx) <br/> |[ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) <br/> [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) <br/> [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) <br/> [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) <br/> [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) <br/> [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) <br/> [VersionUpgrade](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.VersionUpgrade.aspx) <br/> [ViewSwitched](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ViewSwitched.aspx) <br/> |**FormEvents** クラスは、InfoPath フォーム テンプレート自体に固有のイベントを実装します。  <br/> **ContextChanged** <br/> コンテキスト ノードが変更されると発生します。  <br/> **Loading** <br/> フォーム テンプレートが読み込まれた後、ビューが初期化される前に発生します。  <br/> **Merge** <br/> [ **フォームの結合**] コマンドがユーザー インターフェイスから起動される、または  `/aggregate` コマンド ライン スイッチを指定して InfoPath が開始されると発生します。  <br/> **Save** <br/> ユーザー インターフェイスから [ **保存**] または [ **名前を付けて保存**] コマンドが使用される、または [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Save.aspx) クラスの [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SaveAs.aspx) メソッドおよび [SaveAs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) メソッドが使用されると発生します。  <br/> **Sign** <br/> [ **デジタル署名**] ダイアログ ボックスで署名することになる署名データが選択されると発生します。  <br/> **Submit** <br/> ユーザー インターフェイスから [ **送信**] コマンドが使用される、または [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Submit.aspx) クラスの **Submit** メソッドが使用されると発生します。  <br/> **VersionUpgrade** <br/> 開かれているフォームのバージョン番号が、基になっているフォーム テンプレートのバージョン番号よりも古いと発生します。  <br/> **ViewSwitched** <br/> フォームのビューの切り替えが成功した後で発生します。  <br/> |
|[XmlEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.aspx) <br/> |[Changed](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changed.aspx) <br/> [Changing](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changing.aspx) <br/> [Validating](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Validating.aspx) <br/> |フォーム インスタンスの基になっている XML ドキュメントのデータに対する変更によって発生するイベントを実装します。  <br/> **Changed** <br/> フォームの基になっている XML ドキュメントの変更が受け付けられ、 **Validating** イベントが発生した後、発生します。  <br/> **Changing** <br/> フォームの基になっている XML ドキュメントに対する変更が行われた後で、変更が受け付けられる前に発生します。  <br/> **Validating** <br/> フォームの基になっている XML ドキュメントの変更が受け付けられた後、 **Changed** イベントが発生する前に発生します。  <br/> **XmlEvent** クラスは、 [RaiseUndoRedoForChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.RaiseUndoRedoForChanged.aspx) プロパティも実装します。このプロパティは、元に戻す操作またはやり直し操作が実行されたときに **Changed** イベントが発生するかどうかを取得または設定します。    <br/> |
   
> [!NOTE]
>  **Changed** イベントと **Changing** イベントは、フォームの空白ではないフィールドが変更されたときに 1 回だけ発生します。一方、 [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) 名前空間によって提供される InfoPath 2003 と InfoPath 2003 互換のオブジェクト モデルの類似したイベント ( [OnBeforeChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnBeforeChange.aspx) と [OnAfterChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx) ) は、フォームの空白ではないフィールドの変更時に 2 回発生します。つまり、古い値が削除されたときに 1 回、新しい値が挿入されたときにもう 1 回発生します。 
  
## <a name="overview-of-the-eventargs-classes"></a>EventArgs クラスの概要

12 個の各イベントには、イベント ハンドラーに渡される **EventArgs** オブジェクトが関連付けられています。このオブジェクトにより、イベント ハンドラー コードで使用できるイベントの状態情報およびその他の機能が提供されます。次の表に、InfoPath イベント、関連付けられた **EventArgs** オブジェクト、およびオブジェクトのプロパティとメソッドで提供される機能の簡単な説明を示します。オブジェクトの特定のプロパティとメソッドの詳細については、表の **EventArgs** オブジェクトの名前をクリックし、トピックの [メンバー] リンクをクリックしてください。 
  
|**イベント**|**EventsArgs クラス**|**説明**|
|:-----|:-----|:-----|
|**Clicked** <br/> |[ClickedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.aspx) <br/> |コントロール ID を取得します。  <br/> [ **ボタン**] コントロールを含む、フォームの基になる XML ドキュメントで、最も内側の XML ノードに置かれている **XPathNavigator** オブジェクトを取得します。  <br/> |
|**ContextChanged** <br/> |[ContextChangedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.aspx) <br/> |イベントが発生したときに実行されたコンテキスト変更の種類を取得します。  <br/> 操作を元に戻したかやり直したことによって、コンテキスト変更が発生したかどうかを示す値を取得します。  <br/> イベントが発生したコンテキスト ノードに置かれていた **XPathNavigator** への参照を取得します。  <br/> |
|**Loading** <br/> |[LoadingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.LoadingEventArgs.aspx) <br/> |読み込み後にフォームを開くビューを指定します。  <br/> **XmlFormCancelEventArgs** オブジェクトへの参照を取得します。  <br/>  コマンド ライン オプションを使用して、またはフォームを開く URL のクエリ パラメーターを使用して指定された入力パラメーターを含む `/InputParameters` を取得します。  <br/> |
|**Merge** <br/> |[MergeEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.aspx) <br/> |**XmlFormCancelEventArgs** オブジェクトへの参照を取得します。  <br/> 結合操作で結合されるフォームの数を取得します。  <br/> 現在結合されているフォームの、ゼロベースのインデックスを取得します。  <br/> 現在のフォームのみを取り消すのか、または結合操作全体を取り消すのかを判別するために、 **Cancel** プロパティと共に使用する値を取得または設定します。  <br/> 現在結合されているフォームの基になっている XML ドキュメントのルート ノードに配置されている **XPathNavigator** オブジェクトを取得します。  <br/> |
|**Save** <br/> |[SaveEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SaveEventArgs.aspx) <br/> |ユーザーによって要求された保存操作を実行します。  <br/> イベントの取り消しに使用できる **SaveCancelEventArgs** オブジェクトへの参照を取得します。  <br/> イベントに対するイベント ハンドラーで使用するファイル名を取得します。  <br/> 保存操作が "保存" 操作として実行されるか "名前を付けて保存" として実行されるかを取得します。  <br/> |
|**Sign** <br/> |[SignEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.aspx) <br/> |[ **デジタル署名**] ダイアログ ボックスを表示するかどうかを取得または設定します。  <br/> イベントを発生させた署名可能なデータのセットを取得します。  <br/> |
|**Submit** <br/> |[SubmitEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SubmitEventArgs.aspx) <br/> |イベントを取り消す **XmlFormCancelEventArgs** オブジェクトへの参照を取得します。  <br/> |
|**VersionUpgrade** <br/> |[VersionUpgradeEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.VersionUpgradeEventArgs.aspx) <br/> |イベントを取り消す **XmlFormCancelEventArgs** オブジェクトへの参照を取得します。  <br/> アップグレード中のフォーム ドキュメントのバージョン番号を取得します。  <br/> アップグレード中のフォームに関連付けられたフォーム テンプレートのバージョン番号を取得します。  <br/> |
|**ViewSwitched** <br/> |[ViewSwitchedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewSwitchedEventArgs.aspx) <br/> |**ViewSwitchedEventArgs** クラスには、イベントに対して **System.Object** から継承される以外のプロパティとメソッドはありません。  <br/> |
|**Changed** <br/> |[XmlEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) <br/> |現在変更中のノードを返す XPath 式を含む **XPathExpression** オブジェクトを取得します。  <br/> 変更中のノードの新しい値を取得します。  <br/> 削除中のノードの親であるノードを示す **XPathNavigator** オブジェクトを取得します。  <br/> 変更中のノードの元の値を取得します。  <br/> ノードが変更されたときに発生した操作の種類を示す [XmlOperation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlOperation.aspx) 列挙を取得します。  <br/> 変更中のノードを示す **XPathNavigator** オブジェクトを取得します。  <br/> 変更中のノードが、元に戻すまたはやり直す操作の一部であるかどうかを示す値を取得します。  <br/> |
|**Changing** <br/> |[XmlChangingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlChangingEventArgs.aspx) <br/> |イベントに関連付けられた **XmlFormCancelEventArgs** オブジェクトを取得します。  <br/> 上記の **XmlEventArgs** オブジェクトの機能をすべて継承します。  <br/> |
|**Validating** <br/> |[XmlValidatingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) <br/> |指定した値を持つカスタム エラー情報の入った [FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) オブジェクトを作成し、それをフォームの [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) オブジェクトに追加します。  <br/> 上記の **XmlEventArgs** オブジェクトの機能をすべて継承します。  <br/> |
   
## <a name="using-the-eventargs-objects"></a>EventArgs オブジェクトを使用する

イベント ハンドラーを作成する際、InfoPath は、プロジェクトのフォーム コード ファイル内でイベント ハンドラーの宣言を作成します。イベント ハンドラーの宣言内で、InfoPath は、イベント ハンドラーに渡されるパラメーターの名前として **e** を使用します。このパラメーターには、イベント発生時に状態情報とその他の機能を提供するイベント ハンドラーに関連付けられる **EventArgs** オブジェクトが含まれます。 
  
たとえば、[ **開発**] タブの [ **Loading イベント**] をクリックすることで、デザイン モードで **Loading** イベントのイベント ハンドラーを作成する際、InfoPath は、 [LoadingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.LoadingEventArgs.aspx) オブジェクトを受け取るイベント ハンドラーの宣言をフォーム コード ファイルに追加し、次のイベント ハンドラー宣言にコードを追加するためのコード エディターを開きます。 
  
```cs
public void FormEvents_Loading(object sender, LoadingEventArgs e)
{
   // Write your code here.
}
```

```vb
Public Sub FormEvents_Loading(ByVal sender As Object, _
   ByVal e As LoadingEventArgs)
   ' Write your code here.
End Sub
```

イベント ハンドラーのコードを書く際、 **e** パラメーターを通じて渡される **EventArgs** イベント オブジェクトによって実装されるプロパティとメソッドを使用できます。 たとえば、次の **Changing** イベント ハンドラーでは、 [XmlChangingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.NewValue.aspx) オブジェクトの [NewValue](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlChangingEventArgs.aspx) プロパティ ( [XmlEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) クラスから継承) を使用して、変更されたフィールドの値が確認されます。ユーザーがフィールドを変更し、空白にした場合、 [XmlChangingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCancelEventArgs.Message.aspx) オブジェクトの [CancelableArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCancelEventArgs.aspx) プロパティを使用して、 [XmlFormCancelEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlChangingEventArgs.CancelableArgs.aspx) クラスの **Message** プロパティにアクセスし、ユーザーにエラーを表示し、 **XmlFormCancelEventArgs.Cancel** プロパティを **true** に設定してイベントを取り消し、ユーザーが行った変更内容をロールバックします。
  
```cs
public void field1_Changing(object sender, LoadingEventArgs e)
{
   // Determine whether there is a new value.
   if (e.NewValue == "")
   {
      // The value is blank, so display an error message
      // and roll back the changes.
      e.CancelableArgs.Message = 
         "You must supply a value for this field.";
      e.CancelableArgs.Cancel = true;
      return;
   }
}
```

```vb
Public Sub field1_Changing(ByVal sender As Object, _
   ByVal e As LoadingEventArgs)
   ' Determine whether there is a new value.
   If (e.NewValue = "") Then
      ' The value is blank, so display an error message 
      ' and roll back the changes.
      e.CancelableArgs.Message = _
         "You must supply a value for this field."
      e.CancelableArgs.Cancel = True
      Return
   End If
End Sub
```


