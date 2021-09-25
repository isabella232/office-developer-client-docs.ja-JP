---
title: 実行時環境を決定する条件付きロジックを書く
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath での実行 [infopath 2007],実行時環境 [InfoPath 2007],ブラウザーでの実行 [InfoPath 2007],InfoPath 2007,実行時環境を決定する
ms.localizationpriority: medium
ms.assetid: 1a43bbdc-666b-47ef-a5e3-cb477a4deb04
description: Application クラスの Environment プロパティは、Environment オブジェクトへの参照を取得します。これを使用すると、どの実行時の環境 (InfoPath、Web ブラウザー、またはモバイル ブラウザー) を使ってフォームが開かれたかを判断することができます。
ms.openlocfilehash: 347633f0dc13b8b001ca146cd56aa734c0edc8b6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625820"
---
# <a name="write-conditional-logic-that-determines-the-run-time-environment"></a>実行時環境を決定する条件付きロジックを書く

[Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Environment.aspx) クラスの [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) プロパティは、 [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) オブジェクトへの参照を取得します。これを使用すると、どの実行時の環境 (InfoPath、Web ブラウザー、またはモバイル ブラウザー) を使ってフォームが開かれたかを判断することができます。 
  
## <a name="example"></a>例

### <a name="determining-which-runtime-environment-a-form-is-running-in"></a>フォームが実行されている実行時の環境を判断する

[Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) クラスは、フォーム テンプレートを開くために使用された編集環境を判断することができる [IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) プロパティおよび [IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) プロパティを提供します。これらの両方のプロパティが **false** を返す場合、フォーム テンプレートは Microsoft InfoPath エディターで開かれています。いずれかのプロパティが **true** を返す場合、フォーム テンプレートは対応するプロパティのプログラムで InfoPath Forms Services を実行している Microsoft SharePoint Server 2010 上で、適切に構成されたドキュメント ライブラリから開かれています。 [IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) property プロパティの場合は Web ブラウザー、 [IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) プロパティの場合はモバイル ブラウザーです。 
  
次の例では、フォームがブラウザーまたはモバイル ブラウザーで開かれた場合は、field1 ([ **テキスト ボックス**] コントロールにバインドされている) の値が、フォームが開かれた実行時の環境を示す文字列に設定されます。フォームが InfoPath で開かれた場合は、 **System.Windows.Forms.MessageBox.Show** メソッド (このメソッドは、フォームがブラウザーで実行されているときは使用できません) を使用してメッセージ ボックスが表示されます。 
  
> [!IMPORTANT]
> 以下のコード例のフォーム テンプレートを作成するときは、Backstage ビューの [ **新規作成**] タブで [ **空白**] テンプレートを選択します (または、[ **フォームのオプション**] ダイアログ ボックスの [ **互換性**] カテゴリにある、[ **フォームの種類**] ドロップダウン リストの [ **Web ブラウザー フォーム**] を選択します)。 **MessageBox** クラスをサポートするには、Visual Studio 2012 の [ **参照の追加**] ダイアログ ボックスの [ **.NET**] タブで、 **System.Windows.Forms** への参照を追加します。次に、フォーム コード モジュールの宣言セクションで、 **System.Windows.Forms** の **using** または **Imports** ディレクティブを追加します。 
  
```cs
if(this.Application.Environment.IsBrowser)
{
   CreateNavigator().SelectSingleNode(
      "/my:myFields/my:field1", NamespaceManager).
      SetValue("Running in a browser.");
}
else if (this.Application.Environment.IsMobile)
{
   CreateNavigator().SelectSingleNode(
      "/my:myFields/my:field1", NamespaceManager).
      SetValue("Running in a mobile browser.");
}
else
{
   MessageBox.Show("This form is running in the InfoPath editor.");
}
```

```vb
If (Me.Application.Environment.IsBrowser) Then
   CreateNavigator().SelectSingleNode(_
      "/my:myFields/my:field1", NamespaceManager). _
      SetValue("Running in a browser.")
ElseIf (Me.Application.Environment.IsMobile) Then
   CreateNavigator().SelectSingleNode( _
      "/my:myFields/my:field1", NamespaceManager). _
      SetValue("Running in a mobile browser.")
Else
   MessageBox.Show("This form is running in the InfoPath editor.")
End If
```


