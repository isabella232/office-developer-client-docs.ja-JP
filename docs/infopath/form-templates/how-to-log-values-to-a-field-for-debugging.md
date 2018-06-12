---
title: デバッグ用のフィールドに値をログ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5874dc28-1b10-48a3-8287-9474db0b7435
description: InfoPath フォーム テンプレートをデバッグするときは、通常、フォーム内のフィールドに値のログを直接記録し、フォームのテスト セッション中にデバッグ データのレコードを作成すると有効です。次の手順では、マルチライン フィールドを作成し、ヘルパー関数 (フィールドにデバッグ データのログを記録する関数) をフォーム コードに追加する方法について説明します。
ms.openlocfilehash: f763e6b5d14fe5a5b4d9218af4acd0bc05a242af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799129"
---
# <a name="log-values-to-a-field-for-debugging"></a>デバッグ用のフィールドに値をログ

InfoPath フォーム テンプレートをデバッグするときは、通常、フォーム内のフィールドに値のログを直接記録し、フォームのテスト セッション中にデバッグ データのレコードを作成すると有効です。次の手順では、マルチライン フィールドを作成し、ヘルパー関数 (フィールドにデバッグ データのログを記録する関数) をフォーム コードに追加する方法について説明します。
  
## <a name="create-a-multi-line-text-field"></a>複数行のテキスト フィールドを作成します。

1. **テキスト ボックス** コントロールをフォームに追加し、複数の行を表示できるようにサイズを変更します。 
    
2. テキスト ボックスを右クリックし、[ **テキスト ボックスのプロパティ**] をクリックして、[ **表示**] タブの [ **マルチライン**] チェック ボックスをオンにします。 
    
## <a name="add-helper-functions-to-log-debug-information-to-the-field"></a>フィールドにデバッグ情報をログに記録するヘルパー関数を追加します。

1. [ **開発**] タブの [ **コード エディター**] をクリックし、メッセージが表示されたら、フォーム テンプレートを保存します。
    
2. コード エディターで、次の 3 つのヘルパー関数を、フォーム コード ファイル内のパブリック クラスに追加します。
    
   > [!IMPORTANT]
   > [!重要] `debugFieldXpath` 関数の  `AddToDebugField` 変数に設定されている値を、最初の手順で作成したコントロールに連結するフィールド用の正しい XPath 式に更新します。 
  
    ```cs
        private void AddToDebugField(string valueToAdd)
        {
            // Update the value of debugFieldXpath to the XPath of the
            // multi-line field where you want to log debug information.
            string debugFieldXpath = "/my:myFields/my:field1";
            string headerLine = "----------------- " + DateTime.Now + 
                " -----------------" + "\r\n";
            SetDebugFieldValue(debugFieldXpath, headerLine + valueToAdd + 
                "\r\n" + GetDebugFieldValue(debugFieldXpath));
        }
        private string GetDebugFieldValue(string xpath)
        {
            return this.CreateNavigator().SelectSingleNode(xpath, 
                this.NamespaceManager).Value;
        }
        private void SetDebugFieldValue(string xpath, string value)
        {
            this.CreateNavigator().SelectSingleNode(xpath, 
                this.NamespaceManager).SetValue(value);
        }
    ```

    ```vb
        Private Sub AddToDebugField(ByVal valueToAdd As String)
            ' Update the value of debugFieldXpath to the XPath of the 
            ' multi-line field where you want to log debug information.
            Dim debugFieldXpath As String = "/my:myFields/my:field1"
            Dim headerLine As String = "----------------- " _
                &amp; DateTime.Now &amp; " -----------------" &amp; vbCrLf
            SetDebugFieldValue(debugFieldXpath, (headerLine &amp; valueToAdd &amp; vbCrLf) _
                &amp; GetDebugFieldValue(debugFieldXpath))
        End Sub
        Private Function GetDebugFieldValue(ByVal xpath As String) As String
            Return Me.CreateNavigator().SelectSingleNode(xpath, _
                Me.NamespaceManager).Value
        End Function
        Private Sub SetDebugFieldValue(ByVal xpath As String, ByVal value As String)
            Me.CreateNavigator().SelectSingleNode(xpath, _
                Me.NamespaceManager).SetValue(value)
        End Sub
    ```

> [!NOTE] 
> Visual Basic を使用して、追加`Imports Microsoft.VisualBasic.Constants`フォームのコード ファイルの先頭にディレクティブにします。 
  
## <a name="test-the-addtodebugfield-function"></a>AddToDebugField 関数をテストします。

1. [ **開発**] タブの [ **Loading イベント**] をクリックし、次のコード行をイベント ハンドラーに追加します。
    
   ```cs
    AddToDebugField("Form loaded");
   ```

   ```vb
    AddToDebugField("Form loaded")
   ```

2. [ **開発**] タブの [ **ViewSwitched イベント**] をクリックし、次のコード行をイベント ハンドラーに追加します。
    
   ```cs
    AddToDebugField("View switched: " + this.CurrentView.ViewInfo.Name);
   ```

   ```vb
    AddToDebugField("View switched: " &amp; Me.CurrentView.ViewInfo.Name)
   ```

3. [ **ホーム**] タブの [ **プレビュー**] をクリックします。
    
   デバッグ フィールドに 2 つの項目が表示されます。1 つは、フォームが読み込まれたことを示す項目で、もう 1 つは、ビューの名前を示す項目です。これらの例では、フォームを開くときに発生するイベントのイベント ハンドラーを使用しています。ただし、フォームが読み込まれた後は、フォームのコンテキスト内で実行される他のコードからだけでなく、他のイベント ハンドラーからも、 `AddToDebugField` 関数を呼び出すことができます。 
  

