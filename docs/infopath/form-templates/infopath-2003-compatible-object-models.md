---
title: InfoPath 2003 互換オブジェクト モデル
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, object model,InfoPath 2003-compatible object model,object models [InfoPath 2003], compatible with InfoPath 2007,object models [InfoPath 2007], InfoPath 2003 compatible
localization_priority: Normal
ms.assetid: e4511af6-d7e7-44ad-a50d-1b7ee04f8215
description: Microsoft InfoPath は COM (コンポーネント オブジェクト モデル) アプリケーションとして作成されており、外部オートメーションとフォーム テンプレート スクリプトの両方のプログラミング インターフェイスを COM インターフェイスとして公開します。
ms.openlocfilehash: 09ba36b39e520629764bd57a623e8fb490a63a89
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799159"
---
# <a name="infopath-2003-compatible-object-models"></a>InfoPath 2003 互換オブジェクト モデル

Microsoft InfoPath は COM (コンポーネント オブジェクト モデル) アプリケーションとして作成されており、外部オートメーションとフォーム テンプレート スクリプトの両方のプログラミング インターフェイスを COM インターフェイスとして公開します。マネージ コード言語 (Visual C# および Visual Basic) を使用する InfoPath ソリューションの作成をサポートするために、InfoPath セットアップ プログラムによって 3 つの相互運用アセンブリがインストールされます。相互運用アセンブリとは、マネージ コードとアンマネージ コードの仲介役として機能する .NET アセンブリで、COM オブジェクトのメンバーを、対応する .NET マネージ メンバーにマップします。 
  
InfoPath によってインストールされる 3 つの相互運用アセンブリのファイルを以下に示します。
  
- Microsoft.Office.Interop.InfoPath.dll
    
- Microsoft.Office.Interop.InfoPath.SemiTrust.dll
    
- Microsoft.Office.Interop.InfoPath.Xml.dll
    
ここでは、Microsoft.Office.Interop.InfoPath.SemiTrust 相互運用アセンブリによって公開されるオブジェクト モデルについて説明します。このアセンブリは、InfoPath フォーム テンプレート (.xsn) 内からマネージ コード ビジネス ロジックを書いたり実行したりするためだけに使用されます。 
  
Microsoft.Office.Interop.InfoPath と Microsoft.Office.Interop.InfoPath.Xml のアセンブリについては、 [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/en-us/library/microsoft.office.interop.infopath.aspx)と[Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/en-us/library/microsoft.office.interop.infopath.xml)のマニュアルを参照してください。名前空間です。 
  
## <a name="important-installation-information"></a>インストールに関する重要な情報

既定では、InfoPath セットアップ プログラムのインストール オプションで [ **標準**] を選択すると、Microsoft.Office.Interop.InfoPath.SemiTrust アセンブリと Microsoft.Office.Interop.InfoPath.Xml アセンブリのコピーが C:\Program Files\Microsoft Office\Office14 フォルダーにインストールされます。また、Microsoft.Office.Interop.InfoPath アセンブリと Microsoft.Office.Interop.InfoPath.Xml アセンブリがグローバル アセンブリ キャッシュ (GAC) にインストールされます。グローバル アセンブリ キャッシュ (GAC) の内容は、C:\Windows\Assembly フォルダーから見ることができます。 
  
これらのアセンブリがインストールされていない場合は、Microsoft InfoPath が正しくインストールされていることを確認する必要があります。セットアップを実行する前に .NET Framwork 2.0 以降がインストールされていれば、[ **標準**] を選択して InfoPath をインストールすると、InfoPath セットアップ プログラムの [ **.NET プログラミング サポート**] オプションが [ **マイ コンピューターから実行**] に設定されます。コンピューターでこれらの相互運用アセンブリを使用できない場合は, .NET Framework 2.0 以降がインストールされていることを確認する必要があります。その後、[ **コントロール パネル**] の [ **プログラムの追加と削除**] を実行して、[ **.NET プログラミング サポート**] オプションを [ **マイ コンピューターから実行**] に設定します。
  
.NET Framework 2.0 再頒布可能コンポーネントのダウンロードについては、「[Microsoft .NET Framework Version 2.0 再頒布可能パッケージ (x86)](http://www.microsoft.com/downloads/details.aspx?displaylang=en&amp;FamilyID=0856eacb-4362-4b0d-8edd-aab15c5e04f5)」を参照してください。
  
## <a name="the-microsoftofficeinteropinfopathsemitrust-namespace"></a>Microsoft.Office.Interop.InfoPath.SemiTrust 名前空間

Microsoft Office InfoPath 2003 Service Pack 1 および Microsoft Office InfoPath 2003 Toolkit for Visual Studio® .NET がリリースされるまでは、InfoPath フォーム テンプレートのすべてのプログラム ロジックは、Microsoft Script Editor (MSE) の開発環境で書かれた Microsoft JScript または Microsoft VBScript を使用して作成されていました。MSE で書かれたスクリプトは実行時に解釈され、IPEDITOR.dll ダイナミック リンク ライブラリによって公開される COM オブジェクト モデルにアクセスします。
  
プログラム ロジックに Visual C# や Visual Basic のマネージ コード言語を使用するフォーム テンプレートの作成をサポートするために、共通言語ランタイム (CLR) をホストできるようにするための機能が InfoPath に追加され、InfoPath によって公開される COM オブジェクト モデルとマネージ コードとの相互運用を安全な形で実現するための Microsoft.Office.Interop.InfoPath.SemiTrust 相互運用アセンブリが作成されました。InfoPath マネージ コード フォーム テンプレートに適用されるセキュリティ モデルについては、「[コードを含むフォーム テンプレートのセキュリティ モデルについて](about-the-security-model-for-form-templates-with-code.md)」を参照してください。 
  
InfoPath フォーム テンプレートの特定のタスクのマネージ コードを書くプロセスは、同じプログラミング タスクをスクリプトを書いて実行する場合とよく似ていますが、Visual Studio 2012 の [ **オブジェクト ブラウザー**] で **Microsoft.Office.Interop.InfoPath.SemiTrust** 名前空間を表示したときに公開される InfoPath 2003 互換オブジェクト モデルは、スクリプトの場合より、はるかに複雑に見えます。これは、InfoPath 2003 互換オブジェクト モデルをサポートするために使用される .NET Framework の相互運用技術では、COM サーバーのすべてのパブリック インターフェイスに加えて, .NET Framework 自体が必要とする追加のコンストラクトも COM サーバーで公開される必要があるためです。 
  
### <a name="how-com-objects-are-exposed-to-the-infopath-2003-compatible-object-model"></a>InfoPath 2003 互換オブジェクト モデルの COM オブジェクトを公開する方法

JScript、VBScript、Visual Basic などの高水準言語 (.NET バージョンの Visual Basic や Visual C# は含まない) を使用して COM サーバーをネイティブで操作する場合、公開されるオブジェクト モデルは、基になる COM クラスや COM インターフェイスより単純になります。たとえば、これらの言語を使用した場合、InfoPath の **UI** オブジェクトでは 7 つのメソッドのセット (ユーザーにメッセージ ボックスを表示するための **Alert** メソッドなど) が公開されます。 
  
ただし、 **UI** オブジェクトをサポートする基になる COM コンストラクトは、実際には 3 つのエンティティで構成されています。 **UI** と **UI2** という 2 つのインターフェイスと、この 2 つのインターフェイスのメンバーを実装する COM コクラスです。 **UI** インターフェイスに 2 つのバージョンがあるのは、COM フレームワークでは、インターフェイスの実装を呼び出すプログラムやコンポーネントの下位互換性を維持するために、インターフェイスの定義を変更せずにおく必要があるためです。 
  
この例では、InfoPath の最初のリリースのために定義された **UI** インターフェイスによって、 **Alert** メソッドなどの 4 つのメソッドが提供されます。 **UI2** インターフェイスは、InfoPath Service Pack 1 リリースのために定義されたもので、 **UI** インターフェイスの 2 番目のバージョンと見なすことができます。 **UI2** インターフェイスでは、元の **UI** インターフェイスの 4 つのメソッドが継承されているほか、3 つの新しいメソッド ( **Confirm** メソッドなど) が追加されています。スクリプトでもマネージ コードでも、  **** を使用して `XDocument.UI.Confirm` メソッドを呼び出すコード行を書くことができますが、基になるコードで実際に呼び出されるのは、COM コクラスに実装されている **UI2** インターフェイスの **Confirm** メソッドです。 
  
スクリプト環境に公開されるオブジェクト モデルではこれらの詳細が隠されていますが、マネージ コードから COM サーバーを操作する必要がある相互運用アセンブリでは、コクラスと両方のインターフェイスが公開されます。MSE スクリプト環境で使用される単一の **UI** オブジェクトに対して、 **Microsoft.Office.Interop.InfoPath.SemiTrust** 名前空間では次の 3 つのアイテムが公開されます。 
  
- [UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI.aspx) インターフェイス 
    
- [UI2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.aspx) インターフェイス 
    
- [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) コクラス インターフェイス 
    
これら 3 つのインターフェイスのすべてが [ **オブジェクト ブラウザー**] で公開され、この名前空間のクラス ライブラリ ドキュメントにも含まれています。ただし、実際に使用するのは、 **UI** オブジェクトを実装する **UIObject** コクラス インターフェイスと、 **UIObject** コクラス インターフェイスによって実装されるインターフェイスの最新バージョンである **UI2** インターフェイスのメンバーのみです。 **UIObject** コクラス インターフェイスにその親の [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) オブジェクトからアクセスするには、スクリプトの場合と同様に、 [UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx) アクセサー プロパティを使用します。いくつかの重要な例外を除いては、InfoPath の最初のリリースから含まれていて InfoPath Service Pack 1 のリリース時に更新されたすべてのオブジェクトに、このパターンが当てはまります。 
  
**Certificate** オブジェクトなど、InfoPath Service Pack 1 で追加された新しいオブジェクトでは、基本的なパターンは同じですが、状況がいくぶん単純になります。この場合、関係のあるアイテムは 2 つだけです。1 つは、 [CertificateObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.CertificateObject.aspx) コクラス インターフェイス、もう 1 つは、 [CertificateObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Certificate.aspx) コクラス インターフェイスによって実装される最新かつ唯一のインターフェイスである **Certificate** インターフェイスのメンバーです。このオブジェクトに親からアクセスするには、スクリプトから InfoPath COM オブジェクトを使用する場合と同様に、 [Certificate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Certificate.aspx) アクセサー プロパティを使用します。 
  
コレクションのインターフェイスにも同じパターンが当てはまります。ただし、コレクションのコクラス インターフェイスの名前には、"Object" ではなく "Collection" が付きます。たとえば、COM **DataAdapters** コレクションのコクラス インターフェイスの名前は [DataAdaptersCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataAdaptersCollection.aspx) で、このコクラス インターフェイスが実装するインターフェイスは [DataAdapters](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataAdapters.aspx) インターフェイスです。コレクションへのアクセスに [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DataAdapters.aspx) 親オブジェクトの **DataAdapters** アクセサー プロパティを使用する点も同様です。 
  
この命名パターンには 3 つの例外があります。COM **Application** オブジェクトと COM **XDocument** オブジェクトのコクラス インターフェイスの名前には、"Object" が付きません。これらの名前は、対応する COM オブジェクトと同じ [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) および **XDocument** になります。また、 **Application** コクラス インターフェイスと **XDocument** コクラス インターフェイスによって実装されるインターフェイスの名前は、先頭にアンダースコア文字 (_) が付いて、 [_Application2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.aspx) および [_XDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.aspx) になります。3 つ目の例外は、COM **DataObject** オブジェクトです。このオブジェクトのコクラス インターフェイスの名前は、 [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) です。ただし、このコクラス インターフェイスが実装するインターフェイスは、他の InfoPath COM オブジェクトと同様に、 [DataObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.aspx) になります。 
  
### <a name="how-microsoft-xml-core-services-msxml-50-for-microsoft-office-objects-are-exposed-to-the-infopath-2003-compatible-object-model"></a>InfoPath 2003 互換オブジェクト モデルへの Microsoft XML Core Services (MSXML) 5.0 の Microsoft Office のオブジェクトの公開方法

COM サーバーでもある Microsoft XML Core Services (MSXML) によって提供されるオブジェクト モデルのオブジェクトとメンバーのサブセットが、Microsoft.Office.Interop.InfoPath.SemiTrust 相互運用アセンブリによって公開されるインターフェイスでラップされます。これが必要になるのは、InfoPath COM オブジェクト モデルの一部のメンバーが MSXML に依存しており、それらのメンバーに安全な形でアクセスできるようにする必要があるからです。MSXML オブジェクト モデルのオブジェクトやメンバーをラップする **Microsoft.Office.Interop.InfoPath.SemiTrust** 名前空間のインターフェイスの名前は、MSXML COM サーバーによって公開される名前と同じです。ほとんどの場合、これらの名前には、"IXMLDOM" というプレフィックスが付いています。これは、それらが XML Document Object Model (DOM) の操作に使用されるためです。たとえば、フォームの基になる XML ドキュメントへの参照を取得するために使用される [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx) インターフェイスの **DOM** プロパティは、Microsoft.Office.Interop.InfoPath.SemiTrust 相互運用アセンブリによってラップされた [IXMLDOMDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.IXMLDOMDocument.aspx) インターフェイスを返します。 **IXMLDOMDocument** インターフェイスのメンバーを呼び出して使用する方法は、マネージ コードを使用しないフォーム テンプレートでスクリプトを使用する場合と基本的に同じです。 
  
マネージ コード フォーム テンプレートで Microsoft XML Core Services (MSXML) for Microsoft Office オブジェクト モデルのメンバーを使用する方法の詳細については、「[InfoPath 2003 オブジェクト モデルを使用して MSXML および System.Xml を操作する](working-with-msxml-and-system-xml-using-the-infopath-2003-object-model.md)」を参照してください。
  
### <a name="using-intellisense"></a>IntelliSense を使用する

`thisXDocument` 変数と  `thisApplication` 変数は、マネージ コード フォーム テンプレートで InfoPath 2003 互換オブジェクト モデルに対して書かれるほとんどのコードで使用されます。これらの変数は、既定のクラス ファイル FormCode.cs または FormCode.vb の  `_Startup` メソッドで初期化されます。この  `thisXDocument` 変数と  `thisApplication` 変数を使用して、 [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) コクラス インターフェイスと [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) コクラス インターフェイスのメンバーにアクセスすることができます。いずれかの変数の名前を入力し、続けてピリオドを入力すると、IntelliSense のステートメント入力候補機能により、対応するコクラス インターフェイスのメンバーの一覧が表示されます。このように操作を続けることで、使用するオブジェクト モデル メンバーにアクセスできます。 
  
次の単純な例では、 `thisXDocument` 変数を使用して [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) メソッドにアクセスし、  [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Version.aspx) 変数からアクセスした `thisApplication` プロパティを使用して InfoPath アプリケーションのバージョンを表示しています。 
  
```cs
thisXDocument.UI.Alert(thisApplication.Version);
```

```vb
thisXDocument.UI.Alert(thisApplication.Version)
```

### <a name="using-the-class-library-reference-documentation"></a>クラス ライブラリのリファレンス ドキュメントを使用します。

**Microsoft.Office.Interop.InfoPath.SemiTrust** 名前空間のクラス ライブラリ リファレンス ドキュメントの構成は、コクラス インターフェイスと、そのコクラス インターフェイスによって実装される継承インターフェイスとの関係を反映しています。詳細については、このトピックの前方にある「COM オブジェクトが InfoPath 2003 互換オブジェクト モデルに公開されるしくみ」を参照してください。 
  
**Microsoft.Office.Interop.InfoPath.SemiTrust** 名前空間のリファレンス ドキュメントの構成と命名体系は、一見わかりにくく見えますが、そのトピックの構成は、InfoPath に付属の『InfoPath 開発者リファレンス』の一部である『InfoPath オブジェクト モデル リファレンス』と基本的に同じです。 **Application** インターフェイスと **XDocument** インターフェイスのトピックを例外として、その他の COM コクラス インターフェイスのすべてのトピックは、『InfoPath スクリプト リファレンス』の対応する "オブジェクト" および "コレクション" のトピックに対応しています。たとえば、 **Microsoft.Office.Interop.InfoPath.SemiTrust** 名前空間のリファレンス ドキュメントのトピック「UIObject インターフェイス」および「WindowsCollection インターフェイス」は、InfoPath オブジェクト モデル リファレンスのスクリプト リファレンスの同等の内容を持つトピック「UI オブジェクト」および「Windows コレクション」に対応しています。 
  
ただし、トピックの冒頭のインターフェイスの説明に続くコクラス インターフェイスのメンバーへのリンクでは、空のトピックが表示されます。コクラス インターフェイスによって実装されるメンバーの一覧を表示するには、そのコクラスによって継承される最も新しいインターフェイスのトピックを開き、そのメンバーの表を開く必要があります。継承インターフェイスへのリンクは、コクラス インターフェイスのトピックの「解説」セクションの先頭にあります。
  
コード エディターで F1 キーを押した場合の動作は、インターフェイスのメンバーを操作している場合がほとんどなので、F1 ヘルプを呼び出したメンバーが直接表示される以外は、ほとんど同じです。ただし、メンバーがバージョン付きのインターフェイスから実装される場合があるという点で、初めは混乱する可能性があります。たとえば、「 `thisXDocument.UI.Alert`」と入力し、 `Alert` にカーソルを置いて F1 キーを押すと、「UI2.Alert メソッド」というタイトルのトピックが表示されます。これは、 **Alert** メソッドが **UI2** インターフェイスのメンバーの実装であるからです。 
  
### <a name="passing-optional-parameters-to-infopath-object-model-members"></a>InfoPath オブジェクト モデル メンバーに省略可能なパラメーターを渡す

InfoPath 2003 互換オブジェクト モデルのメンバーにオプションのパラメーターが含まれていて、そのパラメーターの値を指定しない場合は、代わりに **Type.Missing** フィールドを渡す必要があります。実際の値を省略する場合に **Type.Missing** フィールドを渡さないと、ビルド エラーが発生します。これは、Visual C# と Visual Basic のどちらで書かれたコードにも当てはまります。たとえば、 [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SelectNodes.aspx) インターフェイスの [SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) メソッドには、  _varEndNode_ と  _varViewContext_ という 2 つのオプション パラメーターが含まれています。これらのオプション パラメーターに対して実際の値を指定しないコード行は、次のようになっている必要があります。
  
```cs
IXMLDOMNode group1 = 
   thisXDocument.DOM.selectSingleNode("/my:myFields/my:group1");
thisXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing);
```

```vb
Dim group1 As IXMLDOMNode = _
   thisXDocument.DOM.selectSingleNode("/my:myFields/my:group1")
thisXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing)
```

### <a name="about-common-language-specification-compliance"></a>については、共通言語仕様に準拠

Microsoft.Office.Interop.InfoPath.SemiTrust アセンブリのすべてのインターフェイスとメンバーは、内部で **CLSCompliant** 属性が **false** に設定されています。リファレンス ドキュメントは一部 **System.Reflection** を使用して生成されるため、各インターフェイスおよびメンバーの説明に、"このインターフェイス/メソッド/プロパティは CLS に準拠していません" という記述が含まれています。しかし、実際には、 [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) 名前空間のほとんどのインターフェイスとメンバーが CLS に準拠しています。 
  
## <a name="see-also"></a>関連項目

- [InfoPath 2003 オブジェクト モデルを使用するフォーム テンプレートの開発でよく行う作業](common-tasks-for-developing-form-templates-using-infopath-object-model.md)
- [コードを含むフォーム テンプレートのセキュリティ モデルについて](about-the-security-model-for-form-templates-with-code.md)
- [InfoPath 2003 オブジェクト モデルを使用してフォーム テンプレートを作成する](creating-form-templates-using-the-infopath-2003-object-model.md)
- [InfoPath 2003 オブジェクト モデルを理解する](understanding-the-infopath-2003-object-model.md)

