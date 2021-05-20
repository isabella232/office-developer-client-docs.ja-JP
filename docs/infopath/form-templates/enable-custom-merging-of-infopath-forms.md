---
title: InfoPath フォームのカスタム結合の有効化
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: f08f9212-af10-1287-477d-adde7674f523
description: Microsoft InfoPath エディターのフォームの結合機能を使用すると、複数のフォームのデータを 1 つのフォームに結合することができます。
ms.openlocfilehash: f79553f7fdf0b59c77a98fd479e0a307e4f2e6a3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537802"
---
# <a name="enable-custom-merging-of-infopath-forms"></a>InfoPath フォームのカスタム結合を有効にする

The **Merge Forms** feature of the Microsoft InfoPath editor is designed to combine the data from multiple forms into a single form. This is also known as data aggregation. If merging forms is enabled, you can click the **File** tab, click **Save &amp; Send**, click **Merge Forms** under **Import &amp; Link**, and then click the **Merge Forms** button to select one or more forms to merge with the currently opened form. The form that is currently open is the target form and the forms selected in the **Merge Forms** dialog box are known as the source forms.
  
フォームの結合によって集計されたデータには、ソース フォームとターゲット フォームのすべてのデータが含まれる場合と、元データの一部のみが含まれる場合があります。既定の動作は次のとおりです。
  
- 繰り返し要素の場合、データはターゲット ドキュメントの対応する場所に挿入されます。これは、ターゲット要素の **MaxOccurs** 属性が 2 以上の場合です。 
    
- 繰り返さない要素 (つまり、 **MaxOccurs** 属性が "1" の要素) の場合、ソース要素の属性がターゲット要素の既存の属性に追加されます。 
    
## <a name="creating-a-custom-transform"></a>カスタム変換の作成

結合対象のフォームが同じ XML スキーマに基づいている場合は、既定の動作で問題なく結合できます。しかし、スキーマが異なるフォームどうしを結合したり、スキーマが同じ場合の既定の動作を上書きするときもあります。このような場合には、結合の集計指示を記載した XSL 変換 (XSLT) を作成します。XSL 変換は、結合時に適用されます。その結果、インポート対象の情報が記載された DOM ドキュメントと、この情報をターゲット ドキュメントにどのように組み込むかを指定した注釈が作成されます。この注釈は、 `http://schemas.microsoft.com/office/InfoPath/2003/aggregation` 名前空間の XML 属性です。
  
XML 属性とそれぞれの値は、各ノードをターゲットの XML ドキュメントにどのように結合するかを明記した集計指示として機能します。次の節では、各属性について説明します。
  
### <a name="select"></a>select

**agg:select** 属性には、ターゲット要素を特定する絶対 XPath 式を指定します。 
  
### <a name="insert"></a>insert

**agg:action** 属性の値 "insert" は、 **agg:select** 属性に指定されたターゲット要素の子としてソース要素を挿入するように InfoPath に指示するものです。ソース要素の子も挿入対象に含められます。 **selectChild** 属性を使用すると、ノード挿入操作の場所を選択できます。 **order** 属性は、ソース要素を既存のターゲット要素の前に挿入するのか、後に挿入するのかを指定します。 **order** 属性を省略した場合は、"after" が既定値として使用されます。 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="insert" agg:order="before">Some Value</my:field1>

```

### <a name="replace"></a>replace

**agg:action** 属性の値 "replace" は、 **select** 属性の参照する各ターゲット要素をソース要素に置き換えることを InfoPath に指示するものです。 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="replace">Some Value</my:field1>
```

### <a name="mergeattributes"></a>mergeAttributes

**agg:action** 属性の値が "mergeAttributes" の場合は、 **select** 属性の参照する各ターゲット要素の属性とソース要素の属性が結合されます。 
  
```XML
<my:PMAwS agg:action="mergeAttributes"
 agg:select="/my:Root/my:PMAwS">
```

### <a name="delete"></a>delete

**agg:action** 属性の値が "delete" の場合は、 **select** 属性の参照する各ターゲット要素がターゲット ドキュメントから削除されます。 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="delete"/>
```

`http://schemas.microsoft.com/office/InfoPath/2003/aggregation` インターフェイスを実装する XSL オブジェクトを表すには、  `http://schemas.microsoft.com/office/infopath/2003/aggregation-target` 名前空間に指定されている属性のほか、   名前空間も使用します。このインターフェイスのメンバーの中で特に有益なのが、 **get-documentElement** です。
  
### <a name="get-documentelement"></a>get-documentElement

**target:get-documentElement** 関数を使用すると、ターゲット ドキュメントのドキュメント オブジェクト モデルにアクセスできます。ターゲット ドキュメントの現在の内容に基づいて結合の操作を変更できます。 
  
```XML
<xsl:when test="function-available('target:get-documentElement')">
    <xsl:variable name="target" select="target:get-documentElement()" />
    <xsl:if test="not(boolean($target/my:Customer[Name="MyName"]))">
        <my:Customer agg:action="insert" agg:select="/my:MergeForms" />
    </xsl:if>
</xsl:when>

```

## <a name="steps-for-creating-a-custom-merge"></a>カスタム結合の作成手順

1. データの結合元の XML ソース ドキュメントの種類を選択します。各種ソース ドキュメントの代表的なサンプルを集めてください。
    
2. 既存の InfoPath フォームの各種 XML ソース ドキュメントに対応した XML スキーマを取り出します。この手順は簡単で、Backstage の [ **発行**] タブの [ **ソース ファイルのエクスポート**] コマンドを使用して XML スキーマをエクスポートするだけです。XML ドキュメントを InfoPath で作成しなかった場合、Microsoft Visual Studio などのツールを使ってサンプルの XML ドキュメントからスキーマを作成できます。または、InfoPath で XML ドキュメントからサンプル フォームを作成し、そのドキュメント構造から InfoPath が導き出したスキーマをエクスポートできます。 
    
3. 各種 XML ソース ドキュメントから結合対象のデータを特定します。 この手順は、ソース フォームとターゲット フォームの両方の要件に大きく依存します。たとえば、ソース フォームからすべてのデータをコピーした方がよい場合があります。一方、フォームの基になる XML ドキュメントから 1 つか 2 つの要素だけをコピーした方がよい場合もあります。結合するデータを特定するときは、ソース ドキュメントとターゲット ドキュメントの内容を十分に把握し、ソース フォームとターゲット フォームの間で要素が論理的にマッピングされるように注意する必要があります。
    
4. 各種 XML ソース ドキュメントに対応した XSL 変換を作成します。 フォーム結合の構成で、この手順に最も時間がかかります。XSL 変換の役割は、ターゲット フォームと結合できる形式に XML ソース ドキュメントを変換することです。XSL 変換を設計するときに、XML ロケーション パスによる結合を使用するのか、InfoPath 集計指示による結合を使用するのかを決定してください。
    
    XSL 変換の作成には、Visual Studio が便利です。Visual Studio には、構文に色を付ける機能や、ドキュメントの概要を参照する機能があります。また、XSL 要素の終了タグを自動的に付与してくれるので、余分なタイピングが不要になり、入力ミスを抑えることができます。メモ帳などのテキスト エディターでも、XSL 変換を作成できます。
    
    まず、恒等変換から始めます。これは、入力と同じ XML ファイルを出力する XSL 変換です。
    
    ```XML
        <?xml version="1.0"?> 
        <xsl:stylesheet version="1.0" xmlns:xsl="https://www.w3.org/1999/XSL/Transform" 
        xmlns:agg="http://schemas.microsoft.com/office/infopath/2003/aggregation" 
        xmlns:target="http://schemas.microsoft.com/office/infopath/2003/aggregation-target" 
        xmlns:my="http://schemas.microsoft.com/office/infopath/2003/myXSD/2003-05-29T20:30:47"> 
            <xsl:template match="/"> 
                <xsl:copy> 
                <xsl:apply-templates select="@* | node()" /> 
                </xsl:copy> 
            </xsl:template> 
            <xsl:template match="@* | node()"> 
                <xsl:copy> 
                <xsl:apply-templates select="@* | node()" /> 
                </xsl:copy> 
            </xsl:template> 
        </xsl:stylesheet>
    ```

    次に、特殊な処理を追加する要素のテンプレート セクションを上書きします。たとえば、次のテンプレートでは  `<src:Task>` 要素を  `<my:field1>` 要素に変換し、 **agg:action** 属性の値に "replace" を設定しています。 
    
    ```XML
        <xsl:template match="src:Task"> 
            <my:field1 agg:select="/my:myFields/my:field1" agg:action="replace"> 
                <xsl:value-of select="."/> 
            </my:field1> 
        </xsl:template>
    ```

5. XSL 変換ファイルとスキーマ ファイルをフォーム テンプレートに追加します。 各種ソース ドキュメントに対応したスキーマを導き出し、また InfoPath がデータを結合できる形に各種ソース ドキュメントを変換する XSL 変換を作成したら、各スキーマと XSL 変換をフォームのリソースとして追加します。[ **データ**] タブの [ **リソース ファイル**] をクリックし、[ **リソース ファイル**] ダイアログ ボックスの [ **追加**] をクリックします。作成したスキーマ ファイルまたは XSL 変換ファイルを表示し、[ **OK**] をクリックします。作成したスキーマ ファイルおよび XSL 変換ファイルごとに、この手順を繰り返します。
    
    追加するスキーマの中で **targetNamespace** 属性を使用している場合には、プロパティ要素をフォームの .xsf ファイルに追加する必要があります。これにより、InfoPath がスキーマの名前空間を認識できるようになります。フォームの .xsf ファイルにアクセスするには、[ **ファイル**] タブの [ **発行**] をクリックし、[ **ソース ファイルのエクスポート**] をクリックします。スキーマ ファイルおよび XSL 変換ファイルの保存場所を選択し、[ **OK**] をクリックします。設計していた InfoPath フォーム テンプレートを閉じます。
    
    抽出したファイルの保存場所を開き、拡張子が .xsf のファイルを探します。通常は、manifest.xsf という名前が付けられています。このファイルをメモ帳で開き、スキーマに対応した  `<xsf:file>` タグを探し、"namespace" プロパティ要素を追加します。これは、次の例で示すように **targetNamespace** を指定するプロパティ要素です。 
    
    ```xml
        <xsf:file name="IndvTasks.xsd"> 
            <xsf:fileProperties> 
                <xsf:property name="fileType" type="string" value="Resource" /> 
                <xsf:property name="namespace" type="string" 
                value="urn:office-microsoft-com:InfoPath-designer-aggregation-IndStatusReport" /> 
            </xsf:fileProperties> 
        </xsf:file>
    ```

6. カスタム結合に対応するようにフォームを準備する最後の手順は、フォームに関連付けられている .xsf ファイルの **importParameters** 要素を更新することです。 

    最初に、.xsf ファイルで `<xsf:importParameters>` タグを見つけます。 フォームに対して作成したスキーマ/ XSL 変換ペアごとに、**xsf:importSource** 要素を **xsf:importParameters** 要素に追加します。 `<xsf:importParameters enabled="yes"> <xsf:importSource name="" schema="IndvTasks.xsd" transform="ImportTasks.xsl"></xsf:importSource> </xsf:importParameters>`。 
    
    **xsf:importSource** 要素の **name** 属性には、ソース XML ドキュメントにあるフォーム テンプレートの名前が含まれています。 通常、これは空白のままにできます。 **schema** 属性には、前の手順でフォーム テンプレートに追加したスキーマ ファイルの名前が含まれています。 **transform** 属性には、スキーマに準拠するフォームを変換するために使用する XML 変換の名前が含まれています。 
    
    カスタム変換は、[Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) イベントで使用するか、または単独で使用することができます。 
    
## <a name="creating-a-custom-merge-in-code"></a>コードによるカスタム結合の作成

[Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) イベント ハンドラーを使用することで、コードによってカスタム結合を作成できます。フォームに関連付けられている .xsf ファイルで、対応する **importParameters** 要素の **useScriptHandler** 属性を指定します。 

マネージ コードの場合は、**[ユーザー設定コードを使って結合する]** をオンにして、Backstage から利用できる **[詳細設定]** カテゴリの **[フォームのオプション]** ダイアログ ボックスで **[編集]** ボタンをクリックすることで、[Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) イベントを有効にすることができます。 
  

