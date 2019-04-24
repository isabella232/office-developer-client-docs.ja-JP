---
title: リッチ テキストと Web サービス
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 53fddc3f-e9d9-db76-6b84-11befdb23fb0
description: Microsoft InfoPath では、フォーム内のリッチ テキスト ボックス コントロールを、Web サービスから受け取った XML 要素にバインドし、リッチ テキスト ボックス コントロールのデータを Web サービスを通じて XML 要素に送信することができます。要素は XHTML (Extensible HyperText Markup Language) 形式に従っている必要があります。たとえば、リッチ テキストが含まれている MyRichTextElement という名前の要素のスキーマであれば、XML スキーマ定義は次のようになります。
ms.openlocfilehash: d10f4a8cedcff43d1c351068859aee0edf607c81
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299847"
---
# <a name="rich-text-and-web-services"></a>リッチ テキストと Web サービス

Microsoft InfoPath では、フォーム内の **リッチ テキスト ボックス** コントロールを、Web サービスから受け取った XML 要素にバインドし、リッチ テキスト ボックス コントロールのデータを Web サービスを通じて XML 要素に送信することができます。要素は XHTML (Extensible HyperText Markup Language) 形式に従っている必要があります。たとえば、リッチ テキストが含まれている  `MyRichTextElement` という名前の要素のスキーマであれば、XML スキーマ定義は次のようになります。 
  
```XML
<xsd:element name="MyRichTextElement"> 
    <xsd:complexType mixed="true"> 
        <xsd:sequence> 
            <xsd:any namespace="https://www.w3.org/1999/xhtml" processContents="lax" 
                minOccurs="0" maxOccurs="unbounded"/> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element>
```

**リッチ テキスト ボックス** コントロールを XHTML 要素にバインドできるようにするには、あらかじめラッパー ノードを使用して要素をラップしておく必要があります。このラッパー ノードは任意の名前空間に属することができます。ラッパー ノードは次のようになります。 
  
```xml
<xhtmlNode xmlns="https:// someNamespace"> 
    <div xmlns="https://www.w3.org/1999/xhtml">Your rich text here</div> 
</xhtmlNode>
```

このトピックでは、XHTML を送受信できる Web サービスを作成する手順と、InfoPath を使用して Web サービス パラメーターにバインドする方法について、その概要を説明します。ここでは、こうした Web サービスを作成するための詳細な手順は説明しません。Web サービスの操作に関する一定の知識を前提としています。
  
## <a name="how-to-design-a-web-service-to-receive-and-send-xhtml"></a>XHTML を送受信するように Web サービスを設計する方法

XHTML データを格納し、サーバー上の XML ファイルで送受信する Web サービスの例を示します。このファイルは out.xml という名前で、XHTML データを格納するデータ ソースとして機能します。 `getXhtml` および  `setXhtml` という 2 つの Web メソッドがあり、クライアント アプリケーションが XHTML データ ソースとのインターフェイスに使用できるように公開されます。  `getXhtml` Web サービス メソッドは **XmlNode** を返します。これには XHTML が格納されており、InfoPath のリッチ テキスト ボックス コントロールにバインドできます。  `setXhtml` Web サービス メソッドは **XmlNode** をデータとして受け取り、out.xml ファイルに格納します。 
  
> [!NOTE]
> [!メモ] これらの Web メソッドでは、 **System.IO** および **System.Xml** 名前空間を参照する **using** ステートメントが必要です。 
  
`getXhtml` Web サービス メソッドは、ドライブ C の Data フォルダーにある out.xml ファイルから返される XML データの読み込みを試みます。ファイルが見つからないか有効な XML が格納されていないために読み込みに失敗した場合は、XHTML 名前空間を参照する空の **DIV** HTML 要素を返します。 
  
```cs
[WebMethod]
public XmlNode getXhtml()  
{  
            // This is the returned XmlDocument upon Query from InfoPath 
            XmlDocument document = new XmlDocument(); 
 
            // Create a wrapping node with the name of the rich text field. 
            // The "https://someNameSpace" can be any arbitrary namespace 
            XmlNode richNode = document.CreateNode 
                        (XmlNodeType.Element, "MyRichTextElement", "https://someNameSpace"); 
 
            // Temporary XmlDocument 
            XmlDocument tempDocument = new XmlDocument(); 
            try 
            { 
                // Read the saved rich text data from the local machine 
                tempDocument.Load(@"c:\Data\out.xml"); 
            } 
            catch (XmlException) 
            { 
                // If the file does not exist or content is not valid XML 
                tempDocument.LoadXml("<div xmlns=\"https://www.w3.org/1999/xhtml\"></div>"); 
            } 
 
            // Add the file content to the xml 
            richNode.AppendChild 
                        (document.ImportNode(tempDocument.DocumentElement, true)); 
 
            return richNode; 
}  

```

`setXhtml` Web サービス メソッドは、InfoPath フォーム上の **リッチ テキスト ボックス** コントロールから XHTML を受け取ります。Web サービスはノード リストには対応していないので、複数の行を含むリッチ テキスト フィールドが Web サービスに送られた場合、Web サービスは 1 行目のみを受け取り、残りは無視します。 
  
サンプルの  `setXhtml` メソッドは、最上位の XML ノードを受信することを前提としています。通常、最上位の XML ノードは **DIV** 要素にラップされます。 **リッチ テキスト ボックス** コントロール内のテキストの書式が設定されていないなどの理由で、受信した XML にラップ要素が含まれていない場合、このメソッドは、渡された XML がテキスト ノードであることが **NodeType** プロパティで示されているかどうかをチェックすることで、そのことを確かめます。XML がテキスト ノードの場合は、 **DIV** 要素を作成し、テキスト ノードの内容を **DIV** にコピーして、Web サービスから送られたテキストを持つ子のテキスト ノードが **DIV** に格納されるようにします。このメソッドが受信した XML はドライブ C の Data フォルダーにある out.xml ファイルに書き込まれます。 
  
> [!NOTE]
> [!メモ] サンプルの  `setXhtml` メソッドは任意のサイズの XHTML データを受け取るように記述されていますが、実用上は、送信されるデータの大きさを必ず確かめ、送信できるデータの上限を設定してください。 
  
```cs
[WebMethod]  
public void setXhtml(XmlNode xn)  
{  
            XmlDocument document = new XmlDocument(); 
 
            if (xn == null) 
            { 
                // If nothing was submitted or the rich text field is empty, 
                // create a DIV that references the XHTML namespace 
                XmlElement div = document.CreateElement("div", "https://www.w3.org/1999/xhtml"); 
                // Copy the node to our own XmlDocument 
                document.AppendChild(div); 
            } 
            if (xn.NodeType == XmlNodeType.Text) 
            { 
                // If plain text is passed in, wrap it in a DIV 
                // that references the XHTML namespace 
                XmlElement div = document.CreateElement("div", "https://www.w3.org/1999/xhtml"); 
                // Copy the text to the DIV. 
                div.AppendChild(document.ImportNode(xn, true)); 
                // Copy the node to our own XmlDocument 
                document.AppendChild(div); 
            } 
            else 
            { 
                // Copy the node to our own XmlDocument 
                document.AppendChild(document.ImportNode(xn, true)); 
            } 
 
            // Save the file to the local machine 
            document.Save(@"c:\Data\out.xml"); 
}  

```

## <a name="how-to-create-an-infopath-form-that-exchanges-data-with-the-sample-web-service"></a>サンプルの Web サービスとデータを交換する InfoPath フォームの作成方法

サンプルの Web サービスをテストするフォームを作成するには、次の手順を実行します。
  
### <a name="to-create-a-form-that-connects-to-the-sample-web-service"></a>サンプルの Web サービスに接続するフォームを作成するには

1. InfoPath フォーム デザイナーを開きます。
    
2. [ **新規作成**] タブの [ **フォーム テンプレート (高度)**] で [ **Web サービス**] をダブルクリックします。
    
3. [ **データ接続ウィザード**] ダイアログ ボックスで、[ **データの受信**] を選択し、[ **次へ**] をクリックします。
    
4. サンプルの Web サービス メソッドのある Web サービスのアドレスを入力し、[ **次へ**] をクリックします。 
    
5. 受信メソッドの場合、操作として [ **getXhtml**] を選択し、[ **次へ**] をクリックします。
    
6. **getXHTML** Web サービス メソッドはパラメーターを受け取らないので、[ **次へ**] をクリックします。
    
7. **[完了]** をクリックします。
    
8. [ **データ**] タブの [ **送信処理**] グループで [ **その他の場所へ**] をクリックし、[ **Web サービス**] をクリックして、同じ Web サービスを送信データに使用します。 
    
9. サンプルの Web サービス メソッドのある Web サービスのアドレスを入力し、[ **次へ**] をクリックします。
    
10. 送信メソッドの場合、操作として [ **setXhtml**] を選択し、[ **次へ**] をクリックします。
    
11. [ **変更**] をクリックし、[ **dataFields**] フォルダー、[ **s0:getXhtmlResponse**] フォルダー、[ **getXhtmlResult**] フォルダーの順に展開し、[ **MyRichTextElement**] 要素を選択して、[ **次へ**] をクリックします。
    
12. [ **完了**] をクリックします。
    
13. [ **フィールド**] 作業ウィンドウで、[ **dataFields**] フォルダーを展開します。 
    
14. [ **s0:getXhtmlResponse**] および [ **getXhtmlResult**] フォルダーを展開し、[ **MyRichTextElement**] 要素をフォーム上にドラッグします。InfoPath によって、 **MyRichTextElement** 要素が XHTML 要素であることが認識され、リッチ テキスト ボックス コントロールを使用してバインドされます。 
    
15. フォームを保存または発行します。
    
フォームをテストするには、フォームを開き、画像、テーブル、書式設定されたテキストなどのリッチ テキストの内容を入力します。リボン上の [ **送信**] をクリックして、リッチ テキストの内容をサーバー上の out.xml ファイルに格納します。[ **表示**] タブの [ **クエリ**] をクリックし、フォーム上の [ **クエリの実行**] ボタンをクリックします。これにより、out.xml ファイルに格納されている XHTML の内容が **リッチ テキスト ボックス** コントロールに表示されます。リッチ テキスト フィールドに複数の行が含まれている場合、Web サービスは 1 行目のみを受け取り、残りは無視します。 
  

