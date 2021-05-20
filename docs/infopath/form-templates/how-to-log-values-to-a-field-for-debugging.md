---
title: デバッグのために値のログをフィールドに記録する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5874dc28-1b10-48a3-8287-9474db0b7435
description: InfoPath フォーム テンプレートをデバッグするときは、通常、フォーム内のフィールドに値のログを直接記録し、フォームのテスト セッション中にデバッグ データのレコードを作成すると有効です。次の手順では、マルチライン フィールドを作成し、ヘルパー関数 (フィールドにデバッグ データのログを記録する関数) をフォーム コードに追加する方法について説明します。
ms.openlocfilehash: 28f2a1ad3c13aefd9f898bdf397c9103df98d3c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431814"
---
# <a name="log-values-to-a-field-for-debugging"></a><span data-ttu-id="7e4c2-104">デバッグのために値のログをフィールドに記録する</span><span class="sxs-lookup"><span data-stu-id="7e4c2-104">Log values to a field for debugging</span></span>

<span data-ttu-id="7e4c2-p102">InfoPath フォーム テンプレートをデバッグするときは、通常、フォーム内のフィールドに値のログを直接記録し、フォームのテスト セッション中にデバッグ データのレコードを作成すると有効です。次の手順では、マルチライン フィールドを作成し、ヘルパー関数 (フィールドにデバッグ データのログを記録する関数) をフォーム コードに追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7e4c2-p102">When debugging an InfoPath form template, it is often useful to log values directly into a field in the form to create a record of debug data during a session of testing the form. The following procedures show how to create a multi-line field, and then add helper functions to the form code that enable you log debug data into that field.</span></span>
  
## <a name="create-a-multi-line-text-field"></a><span data-ttu-id="7e4c2-107">マルチライン テキスト フィールドを作成する</span><span class="sxs-lookup"><span data-stu-id="7e4c2-107">Create a multi-line text field</span></span>

1. <span data-ttu-id="7e4c2-108">**テキスト ボックス** コントロールをフォームに追加した後、複数行を表示できるようにテキスト ボックスのサイズを変更します。</span><span class="sxs-lookup"><span data-stu-id="7e4c2-108">Add a **Text Box** control to the form, and then resize it so that it can display multiple lines.</span></span> 
    
2. <span data-ttu-id="7e4c2-109">テキスト ボックスを右クリックし、**[テキスト ボックスのプロパティ]** をクリックしてから、**[表示]** タブで **[マルチライン]** チェック ボックスをクリックします。</span><span class="sxs-lookup"><span data-stu-id="7e4c2-109">Right-click the text box, click **Text Box Properties**, and then click the **Multi-line** check box on the **Display** tab.</span></span> 
    
## <a name="add-helper-functions-to-log-debug-information-to-the-field"></a><span data-ttu-id="7e4c2-110">フィールドにデバッグ情報のログを記録するヘルパー関数を追加する</span><span class="sxs-lookup"><span data-stu-id="7e4c2-110">Add helper functions to log debug information to the field</span></span>

1. <span data-ttu-id="7e4c2-111">**[開発者]** タブで、**[コード エディター]** をクリックし、ダイアログ ボックスが表示されたら、フォーム テンプレートを保存します。</span><span class="sxs-lookup"><span data-stu-id="7e4c2-111">On the **Developer** tab, click **Code Editor**, and then save the form template if you are prompted.</span></span>
    
2. <span data-ttu-id="7e4c2-112">コード エディターで、次の 3 つのヘルパー関数を、フォーム コード ファイル内のパブリック クラスに追加します。</span><span class="sxs-lookup"><span data-stu-id="7e4c2-112">In the Code Editor, add the following three helper functions to the public class in the form code file.</span></span>
    
   > [!IMPORTANT]
   > <span data-ttu-id="7e4c2-113">`debugFieldXpath` 関数の  `AddToDebugField` 変数に設定されている値を、最初の手順で作成したコントロールに連結するフィールド用の正しい XPath 式に更新します。</span><span class="sxs-lookup"><span data-stu-id="7e4c2-113">Make sure that you update the value set for the  `debugFieldXpath` variable in the  `AddToDebugField` function to the correct XPath expression for the field bound to the control that you created in the first procedure.</span></span> 
  
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
> <span data-ttu-id="7e4c2-114">Visual Basic を使用している場合は、フォーム コード ファイルの一番上のディレクティブに、`Imports Microsoft.VisualBasic.Constants` を追加します。</span><span class="sxs-lookup"><span data-stu-id="7e4c2-114">When using Visual Basic, add  `Imports Microsoft.VisualBasic.Constants` to the directives at the top of the form code file.</span></span> 
  
## <a name="test-the-addtodebugfield-function"></a><span data-ttu-id="7e4c2-115">AddToDebugField 関数をテストする</span><span class="sxs-lookup"><span data-stu-id="7e4c2-115">Test the AddToDebugField function</span></span>

1. <span data-ttu-id="7e4c2-116">**[開発者]** タブで、**[Loading イベント]** をクリックし、次のコード行をイベント ハンドラーに追加します。</span><span class="sxs-lookup"><span data-stu-id="7e4c2-116">On the **Developer** tab, click **Loading Event**, and then add the following line of code to the event handler.</span></span>
    
   ```cs
    AddToDebugField("Form loaded");
   ```

   ```vb
    AddToDebugField("Form loaded")
   ```

2. <span data-ttu-id="7e4c2-117">[ **開発**] タブの [ **ViewSwitched イベント**] をクリックし、次のコード行をイベント ハンドラーに追加します。</span><span class="sxs-lookup"><span data-stu-id="7e4c2-117">On the **Developer** tab, click **View Switched Event**, and then add the following line of code to the event handler.</span></span>
    
   ```cs
    AddToDebugField("View switched: " + this.CurrentView.ViewInfo.Name);
   ```

   ```vb
    AddToDebugField("View switched: " &amp; Me.CurrentView.ViewInfo.Name)
   ```

3. <span data-ttu-id="7e4c2-118">[ **ホーム**] タブの [ **プレビュー**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7e4c2-118">On the **Home** tab, click **Preview**.</span></span>
    
   <span data-ttu-id="7e4c2-p103">デバッグ フィールドに 2 つの項目が表示されます。1 つは、フォームが読み込まれたことを示す項目で、もう 1 つは、ビューの名前を示す項目です。これらの例では、フォームを開くときに発生するイベントのイベント ハンドラーを使用しています。ただし、フォームが読み込まれた後は、フォームのコンテキスト内で実行される他のコードからだけでなく、他のイベント ハンドラーからも、 `AddToDebugField` 関数を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="7e4c2-p103">The debug field should display two entries: one indicating that the form is loaded, and another indicating the name of the view. These examples use event handlers for events that occur as the form is opened. However, after the form is loaded, you can call the  `AddToDebugField` function from other event handlers in addition to any other code running in the context of the form.</span></span> 
  

