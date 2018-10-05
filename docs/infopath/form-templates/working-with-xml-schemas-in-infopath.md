---
title: InfoPath で XML スキーマを使用する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: c1d70e9f-b9fc-7bdb-107e-d0cd8191607b
description: Microsoft InfoPath で作成するフォーム テンプレートでは、InfoPath フォームで入力、編集、出力される XML の構造とデータの検証が XML スキーマ (XSD) を使用して実行されます。InfoPath のフォーム デザイン ウィンドウで作成したすべてのフォーム テンプレートには、実行時の検証に使用される XSD スキーマ ファイル (.xsd) が少なくとも 1 つ含まれています。
ms.openlocfilehash: 25828c3ec21d22a9952452d5a82fe1a3b4bab54c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395505"
---
# <a name="working-with-xml-schemas-in-infopath"></a>InfoPath で XML スキーマを使用する

Microsoft InfoPath で作成するフォーム テンプレートでは、InfoPath フォームで入力、編集、出力される XML の構造とデータの検証が XML スキーマ (XSD) を使用して実行されます。InfoPath のフォーム デザイン ウィンドウで作成したすべてのフォーム テンプレートには、実行時の検証に使用される XSD スキーマ ファイル (.xsd) が少なくとも 1 つ含まれています。
  
> [!NOTE]
> このトピックで説明する内容は、InfoPath エディターでの使用を目的としてフォーム テンプレートをデザインする場合に適用されます。ブラウザー互換のフォーム テンプレートの場合は、XSD スキーマの要件がより厳しくなります。詳細については、ブラウザー互換フォーム テンプレートの XML スキーマに関する MSDN のドキュメントを参照してください。 
  
## <a name="using-externally-authored-xml-schemas"></a>外部で作成された XML スキーマを使用する

InfoPath の外部で作成された XSD スキーマ ファイルを読み込むには、次の手順を実行します。
  
### <a name="to-create-a-form-template-based-on-an-external-schema"></a>外部スキーマに基づいてフォーム テンプレートを作成するには

1. Backstage で [ **新規作成**] をクリックし、[ **フォーム テンプレート (高度)**] の [ **XML またはスキーマ**] をクリックして、[ **フォームのデザイン**] をクリックします。
    
2. **データ ソース ウィザード**で、使用する XSD スキーマ ファイルを指定して [ **次へ**] をクリックし、ウィザードの残りのページの処理を行います。 
    
## <a name="unsupported-xsd-constructs"></a>サポートされていない XSD コンストラクト

ここでは、InfoPath で実行時に処理できない XSD コンストラクトについて説明します。InfoPath のフォーム デザイン ウィンドウでフォーム テンプレートを作成する際は、これらのコンストラクトを使用しないでください。
  
## <a name="entity-and-entities-types"></a>ENTITY 型と ENTITIES 型

**ENTITY** 型と **ENTITIES** 型は、検証にドキュメント型定義 (DTD) が必要ですが、InfoPath は DTD をサポートしていません。InfoPath では、このようなスキーマに基づくフォーム テンプレートはデザインできないため、 **ENTITY** 型の派生元である **NCName** 型を **ENTITY** の代わりに使用することを勧めるエラー メッセージが表示されます。 
  
> [!NOTE]
>  InfoPath のデザイン モード以外の場所でフォーム テンプレートを手動で作成し、このテンプレートで **ENTITY** 型と **ENTITIES** 型を含む XSD を使用する場合、これらの型に必要な DTD が Template.xml ファイルに記述されていれば、フォーム テンプレートが実行時に機能します。 
  
## <a name="required-xsdany-element"></a>必須の xsd:any 要素

**xsd:any** ワイルドカード要素が出現する場合、つまり、 **xsd:any** 要素の **minOccurs** 属性の値がゼロより大きい場合 ("必須の any 要素")、InfoPath でこのスキーマ フラグメントに対する有効なインスタンスを判定して作成することができません。InfoPath では、このようなスキーマ フラグメントを使用するフォームの生成時に、有効なインスタンスを作成できなくてはなりません。スキーマで **xsd:any** 要素が必須となっている場合は、 **データ ソース ウィザード**の実行時に、必須の **xsd:any** 要素の代わりに使用するスキーマ要素を選択する必要があります。 
  
## <a name="elements-with-an-abstract-complex-type"></a>抽象複合型の要素

InfoPath のデザイン モードでは、抽象複合型を使用するスキーマに基づいてフォーム テンプレートをデザインできます。たとえば、 `shippingAddress` という要素の型が  `address` という名前の抽象複合型であり、この抽象複合型に  `USAddress` と  `CanadianAddress` という 2 つの派生型がある場合、InfoPath では、  `shippingAddress` のすべてのインスタンスが、  `shippingAddress` 型の  `USAddress` と  `shippingAddress` 型の  `CanadianAddress` の二者択一として扱われます。この例では、提供されたスキーマに address から派生する型がない場合、InfoPath はこの要件を満たす追加のスキーマを必要とします。 
  
## <a name="xsd-constructs-with-reduced-functionality"></a>機能が制限される XSD コンストラクト

ここでは、InfoPath のフォーム デザイン ウィンドウでフォーム テンプレートを作成する際、使用すると機能が制限される XSD コンストラクトについて説明します。
  
## <a name="substitution-groups"></a>代替グループ

代替グループのメンバーはすべて [ **フィールド**] 作業ウィンドウに表示されます。InfoPath では、代替候補がすべての代替グループからの複数択一として表現されます (定義元の要素も抽象要素でない場合は対象となります)。抽象要素の代替グループがない場合は、代替グループである要素を少なくとも 1 つ含むスキーマを提供するように求められます。 
  
## <a name="unbounded-choice-elements"></a>unbounded の choice 要素

次のスキーマ フラグメントは、unbounded の choice 要素を示しています。
  
```XML
<xsd:choice maxOccurs="unbounded"> 
    <xsd:element name="my_element_1"/> 
    <xsd:element name="my_element_2"/> 
</xsd:choice> 

```

InfoPath では、繰り返し出現する選択肢要素は、[ **フィールド**] 作業ウィンドウに繰り返し選択肢として表示されます。[ **繰り返し選択肢グループ**] というコントロールを使用して、XSD で繰り返し回数が無制限の choice 要素によって定義される、異種混在情報の一覧を表現できます。 
  
## <a name="repeating-sequence"></a>繰り返し回数が無制限の sequence 要素

次のスキーマ フラグメントは、繰り返し回数が無制限の sequence 要素を示しています。
  
```XML
<xsd:sequence maxOccurs="unbounded"> 
    <xsd:element name="my_element_1"/> 
    <xsd:element name="my_element_2" minOccurs="0"/> 
</xsd:sequence> 

```

繰り返し回数が無制限の sequence 要素に必要な子要素が含まれていれば、その XSD を無変更で InfoPath に読み込み、繰り返し出現の sequence 要素に繰り返しセクション コントロールをバインドできます。
  
## <a name="choice-of-model-groups"></a>モデル グループの選択

次のスキーマ フラグメントは、複数のモデル グループを含む choice 要素を示しています。
  
```XML
<xsd:choice> 
    <xsd:element name="my_element_1"/> 
    <xsd:sequence> 
        <xsd:element name="my_element_2"/> 
        <xsd:element name="my_element_3"/> 
    </xsd:sequence> 
</xsd:choice> 

```

InfoPath のデザイン モードでは、このような XSD コンストラクトがそのままサポートされ、フォーム デザイン ウィンドウで変更を加える必要はありません。InfoPath でスキーマの意味が変更されることはありませんが、[ **フィールド**] 作業ウィンドウでは上記の choice 構造体が同等の 1 つの選択肢グループとして簡易表示されます。 
  
## <a name="optional-sibling-with-same-qualified-name"></a>修飾名が同じ省略可能な兄弟要素

次のスキーマ フラグメントは、修飾名 (`QName`) が同じ省略可能な兄弟要素を示しています。
  
```xml
<xsd:sequence> 
    <xsd:element name="my_element_1" minOccurs="0"/> 
    <xsd:element name="my_element_2"/> 
            <xsd:element name="my_element_1"/> 
</xsd:sequence> 

```

これらのノードを取得するための **XPath** 式は、InfoPath のフォーム デザイン ウィンドウで XML インスタンスの候補をすべて考慮する必要があるため、複雑になる場合があります。InfoPath では、正しい **XPath** バインディングを作成できない可能性があるスキーマ部分は公開されません。無視されるスキーマ部分については、警告が表示されます。 
  
## <a name="xsd-constructs-with-special-meaning-in-infopath"></a>InfoPath で特別な意味を持つ XSD コンストラクト

ここでは、デザイン モードでフォーム テンプレートを作成する際、使用すると特別な意味が発生する XSD コンストラクトについて説明します。これらのコンストラクトをスキーマで使用して、特定の動作を有効にする方法についても説明します。
  
## <a name="adding-new-element-fields-and-groups-with-the-fields-task-pane"></a>[フィールド] 作業ウィンドウで新しい要素フィールドとグループを追加する

デザイン時に [ **フィールド**] 作業ウィンドウを使用して新しい要素フィールドやグループを追加できる構造を、スキーマに含めておくことができます。そのようにするには、省略可能な unbounded の **xsd:any** 要素を使用してスキーマで要素宣言をし、xsd:any 要素の namespace 属性に **##any** ワイルドカードを指定します。これにより、デザイン時に [ **フィールド**] 作業ウィンドウを使用して、その要素に新しい要素フィールドやグループを追加できるようになります。たとえば、次の要素には新しいコンテンツを追加できます。 
  
```XML
<xsd:element name="open"> 
    <xsd:complexType> 
         <xsd:sequence> 
             <xsd:any minOccurs="0" maxOccurs="unbounded" namespace="##any"processContents="lax"/> 
         </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="adding-new-attribute-fields-with-the-fields-task-pane"></a>[フィールド] 作業ウィンドウで新しい属性フィールドを追加する

要素の場合と同様に、namespace 属性に **##any** ワイルドカードを指定した **anyAttribute** 要素を使用して属性を宣言します。デザイン時に、[ **フィールド**] 作業ウィンドウを使用して、このスキーマ属性に新しいコンテンツを追加できます。 
  
```XML
<xsd:element name="open"> 
    <xsd:complexType> 
        <xsd:anyAttribute namespace="##any" processContents="lax"/> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="storing-xml-signatures-in-the-data-source"></a>データ ソースに XML 署名を格納する

実行時にユーザーのデジタル署名をフォームに入力できるようにするには、ユーザーがフォームに署名したときに作成される XML 署名 (デジタル署名) 情報の格納用として、signature という名前の要素をデータ ソースのスキーマで宣言する必要があります。この宣言は、 **xsd:any** 要素を使用して行い、その namespace 属性にはワイルドカード文字を使用して XML 署名の名前空間を指定します (例: "https://www.w3c.org/2000/09/xmldsig#")。 
  
```XML
<xsd:element name="signature"> 
    <xsd:complexType> 
        <xsd:sequence> 
            <xsd:any namespace="https://www.w3c.org/2000/09/xmldsig#"  
             processContents="lax" minOccurs="0" maxOccurs="unbounded"/> 
        <xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="binding-a-field-to-a-rich-text-box-control"></a>リッチ テキスト ボックス コントロールにフィールドをバインドする

 InfoPath の **リッチ テキスト ボックス** コントロールは、汎用的な XHTML を生成します。したがって、フォーム インスタンスの XML では任意の数のテキスト ノードと XHTML ノードが有効であることが、スキーマで指定されている必要があります。そのように指定するには、次の XSD コンストラクトを使用します。 
  
```XML
<xsd:element name="xhtml"> 
    <xsd:complexType mixed="true"> 
        <xsd:sequence> 
            <xsd:any minOccurs="0" maxOccurs="unbounded" namespace="https://www.w3.org/1999/xhtml" processContents="lax"/> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

> [!NOTE]
> InfoPath では、スキーマ ファイル (.xsd) の内容が変更されることはありませんが、論理的にスキーマ ファイルがデザイン用のサブセットとして扱われることはあります。スキーマ ファイルは、デザイン時も実行時もフォーム テンプレート内では必ず無変更のまま維持されます。 
  
## <a name="debugging-common-xsd-errors"></a>一般的な XSD エラーをデバッグする

外部で作成された XSD ファイルを読み込んで、InfoPath フォーム デザイン ウィンドウでフォーム テンプレートを作成する場合、MSXML エラー メッセージと InfoPath エラー メッセージの 2 種類のエラー メッセージのどちらかが表示されることがあります。MSXML のエラー メッセージは、InfoPath のエラー メッセージ ダイアログ ボックスの [ **詳細**] セクションに表示され、冒頭には必ず、エラーの原因となっているスキーマ ファイルの名前またはパスに関する情報が示されます。InfoPath では、XSD スキーマの有効なコンストラクトの一部がサポートされていません。これらのコンストラクトについては、「サポートされていない XSD コンストラクト」で前述しています。ここでは、スキーマを InfoPath に正常に読み込めない結果を招く一般的なエラーの一部について説明します。 
  
## <a name="the-xsd-namespace-declaration"></a>XSD 名前空間の宣言

すべての W3C 標準と同様に、XML スキーマ (XSD) も長期にわたる検討プロセスを経て勧告となるに至っています。多数の草案が出され、絶えず変化する草案段階の各標準に基づいて数々の XSD ファイルが記述されました。この勧告プロセスの間に、Microsoft は XML-Data Reduced (XDR) と呼ばれる独自のスキーマ言語を開発し、MSXML 3.0 に組み込みました。MSXML 4.0 のリリース以降は、Microsoft XML Core Services で XSD の勧告をサポートしています。スキーマ作成用の多数のプログラムが、XSD の勧告を待たずに開発されました。これらの古いバージョンのプログラムでは、InfoPath が依存する MSXML 5.0 インフラストラクチャでサポートされていない旧式の XSD ファイルが作成される可能性があります。
  
XSD ファイルが XSD 勧告を確実にサポートするようにするには、次の XML 名前空間宣言を \<schema\> タグに含めます。
  
```XML
xmlns:xsd="https://www.w3.org/2001/XMLSchema"
```

すべての XML 名前空間宣言と同様、XML プレフィックス (この場合は 'xsd') には、有効なプレフィックス文字列を任意に指定できます。実際に使用される一般的なプレフィックスとしては、'xsd'、'xs'、'' (プレフィックスなし) などが挙げられます。MSXML では、通常、この名前空間宣言がない場合、ルートが正しく定義されていないという内容のエラーが報告されます。
  
## <a name="importing-and-including-schemas"></a>スキーマをインポートおよびインクルードする

XSD スキーマは拡張が可能で、他のスキーマをインポートおよびインクルードできます。一般に、 **targetNamespace** 属性で指定されているスキーマが現在のスキーマと異なる場合は、スキーマをインポートします。 **targetNamespace** 属性に指定されているスキーマが現在のスキーマと同じ場合は、スキーマをインクルードします。 
  
スキーマのインポートとインクルードのセマンティクスは次のとおりです。
  
```XML
<xsd:import namespace = "[anyURI]" schemaLocation = "[anyURI]"/> 
<xsd:include schemaLocation = "[anyURI]"/> 

```

**schemaLocation** 属性がない場合 (一部のコンバーターで起こることがあります)、MSXML でスキーマ ファイルが見つからないためエラーが報告されます。このエラーが表示された場合は、schemaLocation 属性に指定されているリソースまたは場所に、フォーム テンプレートのユーザーがアクセス可能かどうかも確認してください。 **schemaLocation** 属性で参照されているサーバーまたはディレクトリが停止しているか存在しない場合、またはユーザーにアクセス許可が割り当てられていない場合は、当然のことながらエラーが発生します。また、インポートまたはインクルードされるスキーマがすべて有効なスキーマであることも確認する必要があります。 
  
> [!NOTE]
> **schemaLocation** 属性に起因するエラーが問題となるのは、InfoPath でスキーマを最初にインポートするとき、つまり、既存のスキーマに基づいて初めてフォームのデザインを開始するときに限られます。それ以降は、InfoPath では、フォーム テンプレートに格納されているスキーマ ファイルのキャッシュ済みバージョンが使用されます。 
  
スキーマをインポートする場合は、そのスキーマで **targetNamespace** 属性が指定されていなければ、namespace 属性を空にすることができます。一般に、インポート時の名前空間は、インポートするスキーマに指定されている **targetNamespace** に一致しなければなりません。 
  
## <a name="nondeterministic-schemas"></a>非決定論的スキーマ

InfoPath が依存する MSXML 5.0 インフラストラクチャは、非決定論的なスキーマを確実に検出し、このようなスキーマについて警告エラーを報告しますが、このときのエラー メッセージには、エラーの原因となっているスキーマ部分を示す行番号は表示されません。ここでは、XSD スキーマ ファイルが決定論的であることが重要である理由と、非決定論的とはどういう意味かを説明します。また、一般に陥りやすいエラーについても説明します。
  
XSD スキーマの存在意義は、XML のデータ構造と型のセマンティクスを検証することにあります。この目的を果たすために、検証システム (この場合は MSXML 5.0) では XML ノードを XSD 宣言に対応付ける必要があります。この対応付けを行わないと、検証システムで検証を遂行することができません。この対応付けを確実に行える場合、そのスキーマは決定論的であると見なされます。対応付けを不可能にする XML インスタンスが 1 つでもある場合、スキーマは非決定論的ということになります。
  
次に、非決定論的なスキーマの例を示します。
  
```XML
<xsd:element name="file_Information"> 
    <xsd:complexType> 
        <xsd:sequence> 
            <xsd:element name="file_name"/> 
            <xsd:choice> 
                <xsd:element name="file_path"/> 
                <xsd:sequence> 
                    <xsd:element name="file_path" minOccurs="0"/> 
                    <xsd:element name="URI"/> 
                </xsd:sequence> 
            </xsd:choice> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

この XSD セグメントが非決定論的である理由を説明するために、次の XML フラグメントをこのスキーマで検証する場合を想定します。
  
```XML
<file_Information> 
    <file_name>my_Schema.xsd</file_name> 
    <file_path>c:\xsd</file_path> 
</file_Information> 

```

この XML フラグメントでは、*\<file_path\>* 要素が、choice 要素宣言の最初の部分を出所とする必須ノードなのか、choice 要素宣言の 2 番目の部分を出所とする省略可能なノードなのかが判然としません。 この区別は、次の理由で重要になってきます。 
  
1. この XML フラグメントが choice 要素宣言の最初の部分に照らして検証される場合、XML はスキーマに対して有効と判断されます。
    
2. XML フラグメントが choice 要素宣言の第 2 の部分に照らして検証される場合、必須の \<URI\> ノードがないため、スキーマは有効ではないと判断されます。 
    
XSD 検証システムによっては、有効なパスが存在することから、このスキーマに照らした検証で誤った判断が下される場合がありますが、MSXML はより厳密であり、スキーマが非決定論的であるというエラーを報告します。
  
以降では、非決定論的なスキーマの例をさらにいくつか説明します。まず、省略可能な要素について説明します。このようなケースは、XDR と XSD の 2 つのスキーマ言語で既定の基数が異なることから、XDR から XSD へのコンバーターに起因してよく生じます。最初に検討すべきケースは、 **xsd:choice** 要素と **xsd:sequence** 要素を使用して宣言される省略可能な要素です。 **xsd:sequence** 要素内で宣言される省略可能な要素は、通常は適切に検証されますが、次の例に示すように、同じ名前の複数の要素が間に省略可能な要素のみを挟んで出現する場合は例外となります。 
  
```XML
<xsd:element name="container"> 
    <xsd:complexType> 
        <xsd:sequence> 
            <xsd:element ref="aNode" /> 
            <xsd:element ref="anotherNode" minOccurs="0"/> 
            <xsd:element ref="aNode" /> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

このスキーマ フラグメントが非決定論的である理由を説明するために、次の有効な XML フラグメントについて考えることにします。
  
```XML
<container> 
    <aNode/> 
    <aNode/> 
    <anotherNode/> 
</container> 

```

`<aNode>` 要素の前に、1 回しか出現してはならない  `<anotherNode>` 要素が 2 回出現しているため、このフラグメントは明らかに無効です。 
  
ここで、次の XML インスタンスを検証する場合を考えます。
  
```XML
<container> 
    <aNode/> 
    <aNode/> 
</container> 

```

この場合の課題は、このインスタンスが有効かどうかをどのように判定するかです。1 回しか出現してはならない  `<aNode>` 要素が 2 回出現しているのか、それとも、それぞれ許容される  `<aNode>` 要素が 1 回ずつ出現しているのか、これだけでは判断できません。十分な判断材料がないため、このスキーマは非決定論的ということになります。 
  
同様に、 **xsd:choice** 要素内で宣言される省略可能要素も、通常は問題になります。次の簡単な例では、choice が 1 回出現しているが省略可能要素が存在しないのか、それとも一度も出現していないのか判断できません。 
  
```XML
<xsd:choice> 
    <xsd:element name="node" minOccurs="0"/> 
</xsd:choice> 

```

問題となる例として最後に説明するのは、 **xsd:sequence** 要素の後に、  `<xsd:any namespace="##other"/>` のように、名前空間が定義されていない **xsd:any** 要素を使用する場合です。このコンストラクトが省略可能な要素の後に続く場合は特に注意が必要です。前述の例をここでも使用し、次に示すように最後のノードのみを **xsd:any** 要素に置き換えて考えると、非決定論的かどうかに関する前述の説明がすべてここでも当てはまることがわかります。 
  
```XML
<xsd:element name="container"> 
    <xsd:complexType> 
        <xsd:sequence> 
            <xsd:element ref="aNode" /> 
            <xsd:element ref="anotherNode" minOccurs="0"/> 
            <xsd:any />     
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="illegal-enumeration-values"></a>無効な列挙値

XSD スキーマは、通常、実際のインスタンス ドキュメントが検証されるまでは、どのような型検証も実行しません。ただし、スキーマに列挙体が含まれる場合は例外です。この場合は、列挙値が適切なノード値かどうかが列挙型に照らして検証されます。次に、2 つの例を紹介します。
  
```XML
<xsd:simpleType name="showTimes"> 
    <xsd:restriction base="xsd:time"> 
        <xsd:enumeration value="18:30:00"/> 
        <xsd:enumeration value="20:45:00"/> 
        <xsd:enumeration value="eleven o'clock"/> 
    </xsd:restriction> 
</xsd:simpleType> 

```

このスキーマは、"eleven o'clock" が **xsd:time** 型の要素に対して有効な値ではないため無効です。
  
これよりも複雑な例を次に示します。
  
```XML
<xsd:simpleType name="concession"> 
    <xsd:restriction base="xsd:NMTOKEN"> 
        <xsd:enumeration value="GummyBears"/> 
        <xsd:enumeration value="SnowCaps"/> 
        <xsd:enumeration value="M&Ms"/> 
    </xsd:restriction> 
</xsd:simpleType> 

```

この例が正しくないことを理解するには、 **xsd:NMTOKEN** 型がどのように定義されているかを理解する必要があります。W3C によるデータ型仕様では、 **NMTOKEN** 型は「An NMTOKEN (name token) is any mixture of name characters (NMTOKEN (名前トークン) は名前文字の任意の組み合わせとする)」と定義されています。 
  
さらに掘り下げて調べると、'&' が有効な名前文字ではないため、"M&Ms" は **NMTOKEN** 型として有効ではないことがわかります。 
  
## <a name="empty-sequence-or-choice-elements"></a>空のシーケンスまたは選択要素

MSXML では、次の例に示すような、空の **xsd:choice** 要素または **xsd:sequence** 要素を含むスキーマ宣言について、エラーが報告される場合があります。 
  
```XML
<xsd:element name="emptyContainer"> 
    <xsd:complexType> 
        <xsd:choice /> 
    </xsd:complexType> 
</xsd:element> 

```

この問題は、空の  `<xsd:choice />` タグを削除することで解決します。 
  
## <a name="regular-expressions"></a>正規表現

MSXML 5.0 では、読み込み時に正規表現パターンの検証で問題が生じる場合があります。正規表現は複雑になる場合があるため、慎重に使用する必要があります。XSD パーサーはどれも皆、柔軟な正規表現言語を採用しているように見えますが、それは、公式の XSD 正規表現言語に加えて、他の正規表現言語の要素も実装しているからです。InfoPath のフォーム デザイン ウィンドウで正規表現の解析に問題が生じる場合は、InfoPath で生成されるサンプル データが無効であるか、まったく生成されていないことが考えられます。これはデザイン時には、サンプル データが書式設定にしか使用されないため問題にはなりません。ただし、MSXML がサポートしていない正規表現を使用する場合は、ユーザーがフォームに記入する際に、InfoPath でその正規表現に照らして値を検証できません。「[XML Schema Part 0: Primer Second Edition](https://www.w3.org/TR/xmlschema-0/)」では、XSD 正規表現のサポート内容について説明しています。XSD 正規表現と Unicode レベル 1 の正規表現の詳細については、「[Unicode Regular Expressions (英語)](https://www.unicode.org/reports/tr18/)」を参照してください。 
  
## <a name="targetnamespace-attribute-issues"></a>targetNamespace 属性に関する問題

XSD の興味深い点として、 **targetNamespace** 属性では既定で最上位の宣言のみ参照されるが、  `attributeFormDefault=qualified` および  `elementFormDefault=qualified` を設定すると既定の動作を上書き変更できることが挙げられます。例として、次の XSD を想定します。 
  
```XML
<xsd:schema xmlns:xsd="https://www.w3.org/2001/XMLSchema" targetNamespace="https://ns" > 
    <xsd:element name="root"> 
        <xsd:complexType> 
            <xsd:sequence> 
                <xsd:element name="local"/> 
            </xsd:sequence> 
        </xsd:complexType> 
    </xsd:element> 
</xsd:schema> 

```

また、XML インスタンス ドキュメントは次の例のようになります。
  
```XML
<ns:root xmlns:ns="https://ns"> 
    <local/> 
</ns:root> 

```

ローカル定義では、名前空間による修飾は既定で無効なため、ターゲットの名前空間の指定は不要です。ただし、ローカル定義をグローバルに変更する場合は、参照先 (ref) を名前空間プレフィックスで修飾する必要があります。たとえば、次のスキーマは正しくありません。
  
```XML
<xsd:schema xmlns:xsd="https://www.w3.org/2001/XMLSchema" targetNamespace="https://ns" > 
    <xsd:element name="root"> 
        <xsd:complexType> 
            <xsd:sequence> 
                <xsd:element ref="global"/> 
            </xsd:sequence> 
        </xsd:complexType> 
    </xsd:element> 
 
    <xsd:element name="global"/> 
</xsd:schema> 

```

"global" は名前空間 "https://ns" 内にあるため、このスキーマは正しくありません。既定の名前空間は "https://ns" ではないため、単純に ref="global" と指定しただけでは正しく認識されません。この問題を解決するには、ターゲットの名前空間のプレフィックスを追加し、すべてのグローバル参照と型の使用時にこのプレフィックスを使用する必要があります。修正後のスキーマは次のようになります。
  
```XML
<xsd:schema xmlns:xsd="https://www.w3.org/2001/XMLSchema"  
    xmlns:ns="https://ns" targetNamespace="https://ns" > 
    <xsd:element name="root"> 
        <xsd:complexType> 
            <xsd:sequence> 
                <xsd:element ref="ns:global"/> 
            </xsd:sequence> 
        </xsd:complexType> 
    </xsd:element> 
 
    <xsd:element name="global"/> 
</xsd:schema> 

```

スキーマで **targetNamespace** 属性が指定されている場合は、すべてのグローバル参照を適切な名前空間プレフィックスで修飾してください。 
  
## <a name="xml-processing-instruction-encoding-unicode-vs-ansii"></a>XML 処理命令でのエンコーディング (Unicode または ANSII) の指定

XML は、Unicode 文字セットのみをサポートしています。したがって、ANSII 文字を使用するファイルを保存すると情報が失われる可能性があります。ただし、この特定の用途では、ファイルを UTF-16 形式で保存する必要はありません。XML リーダーの実装コストを削減するために、XML 作成者は使用するエンコーディングを最上位の処理命令タグで指定する必要があります。たとえば、次のような処理命令を指定します。
  
```XML
xml version="1.0" encoding="UTF-8"
```

この処理命令タグでは、ファイルのエンコーディングとして UTF-8 が指定されています。ファイル内のエンコーディングは、処理命令タグで指定したエンコーディングと同一にする必要があります。ファイルのエンコーディングは、ファイル内のバイトを調べて Unicode のバイト オーダー マークを探すことにより確認できます。ただし、それよりも簡単な方法があります。XSD スキーマを開く際に問題が生じる場合は、エンコーディングとして "UTF-8" を指定し、スキーマをメモ帳などのテキスト エディターで開いてから、UTF-8 エンコーディングでファイルを保存します (メモ帳には、[ **名前を付けて保存**] ダイアログ ボックスに [ **エンコード**] ドロップダウン リストがあります)。それでもファイルを開く際に問題がある場合、原因はエンコーディングではありません。 
  
## <a name="maxoccurs-attribute-inside-the-xsdall-element"></a>xsd:all 要素内の maxOccurs 属性

XML Schema 勧告における非決定論の定義に基づくと、 **xsd:all** 要素内の **xsd:element** 要素の **maxOccurs** 属性に対して有効な値は 1 のみになります。たとえば、次は正しい例です。 
  
```XML
<xsd:all> 
    <xsd:element name="x" minOccurs="0"/> 
    <xsd:element name="docs" minOccurs="0"/> 
</xsd:all> 

```

しかし、次の例は正しくありません。
  
```XML
<xsd:all>     
    <xsd:element name="x" minOccurs="0" maxOccurs="unbounded"/> 
    <xsd:element name="docs" minOccurs="0" maxOccurs="unbounded"/> 
</xsd:all> 

```

この例が正しくない理由は、 `<x/>` が 2 回出現する場合に、この例の単一の宣言に対応しているのか、この宣言とは別の無効な定義に対応しているのかを検証システムで判断できないためです。同様に、  `<xsd:all>` タグ内に同じ名前の要素を 2 つ含めることもできません。 
  
これは、任意の数の  `<x/>` ノードと  `<docs/>` ノードを任意の順序で親要素内に含められるという点で興味深い例です。このままでは無効ですが、別の方法で記述すれば正しい構造になります。次の例に示すように **xsd:choice** 要素を使用すると、意図した結果を得ることができます。 
  
```XML
<xsd:choice minOccurs="0" maxOccurs="unbounded"> 
    <xsd:element name="x" /> 
    <xsd:element name="docs" /> 
</xsd:choice> 

```

## <a name="how-to-edit-or-author-an-xsd-for-infopath"></a>InfoPath 用に XSD を編集または作成する方法

ここでは 2 つの例を使用して、InfoPath で特定の結果を得られるようにスキーマを編集または作成する方法を示します。
  
## <a name="allowing-user-defined-elements-to-be-inserted-in-the-fields-task-pane"></a>[フィールド] 作業ウィンドウにユーザー定義の要素を挿入できるようにする

[ **フィールド**] 作業ウィンドウで親要素の下にユーザー定義の要素を表示できるようにする場合は、該当する親要素の下に **xsd:any** 要素を挿入する必要があります。  `<your_node_name>` 内にユーザー定義の要素を挿入できるようにする場合は、次のような XSD 宣言が必要です。 
  
```XML
<xsd:element name="your_node_name"> 
    <xsd:complexType> 
        <xsd:sequence> 
            <xsd:any namespace="##any | ##other"  
                minOccurs="0" maxOccurs="unbounded"/> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

ユーザー定義の属性を使用できるようにする場合は、要素宣言に  `<xsd:anyAttribute namespace="##any | ##other"/>` を追加する必要があります。 
  
## <a name="allowing-rich-text-elements-to-be-bound-in-infopath-design-and-edit-modes"></a>InfoPath のデザイン モードと編集モードでリッチ テキスト要素をバインドできるようにする

**Rich Text Box** コントロールにバインドできるように要素を宣言する場合は、次の例に示すように、namespace 属性を "****" に設定した https://www.w3.org/1999/xhtml 要素を含める必要があります。 
  
```XML
<xsd:element name="your_node_name"> 
    <xsd:complexType mixed="true"> 
        <xsd:sequence> 
            <xsd:any namespace="https://www.w3.org/1999/xhtml"  
                minOccurs="0" maxOccurs="unbounded"/> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="conclusion"></a>終わりに

外部で作成された XML スキーマ (.xsd) ファイルに基づく XML フォーム ソリューションのデザインに関する InfoPath のサポートを有効活用することで、業界標準のスキーマまたは所属する会社や組織で作成したカスタム スキーマと連携するフォーム テンプレートを作成できます。この記事で解説した内容を参考にして、InfoPath と互換性のあるカスタムの XSD スキーマ ファイルを作成し、外部で作成された XSD ファイルを InfoPath のデザイン環境に読み込む際によく発生する問題を解決できます。
  
## <a name="see-also"></a>関連項目

- [W3C XML スキーマ](https://www.w3.org/XML/Schema)
- [W3C XML Schema Primer](https://www.w3.org/TR/xmlschema-0/)
- [W3C XML Schema Structures Reference (英語)](https://www.xml.com/pub/a/2000/11/29/schemas/structuresref.html)
- [W3C XML Schema Datatypes Reference (英語)](https://www.xml.com/pub/a/2000/11/29/schemas/dataref.html)
- [XML Schema Tutorial (英語)](https://www.w3schools.com/xml/schema_intro.asp)
- [データ プラットフォーム デベロッパー センター (英語)](https://msdn.microsoft.com/xml/default.aspx)

