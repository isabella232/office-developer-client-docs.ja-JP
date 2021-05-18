---
title: Microsoft Office InfoPath プライマリ相互運用機能アセンブリについて
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2007、プライマリ相互運用機能アセンブリ、InfoPath プライマリ相互運用機能アセンブリ、PIA [InfoPath 2007]、プライマリ相互運用機能アセンブリ [InfoPath 2007]
localization_priority: Normal
ms.assetid: 1b3ae03c-6951-49e4-a489-4712d3f7ba72
description: Visual C# や Visual Basic などのマネージ コード言語を使用する InfoPath ソリューションの作成をサポートするために、InfoPath セットアップ プログラムの .NET プログラミングサポート オプションは、3 つの相互運用機能アセンブリをインストールします。
ms.openlocfilehash: 51773ad46b1371c410c4249e13a489f0c5550cd1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310137"
---
# <a name="about-the-microsoft-office-infopath-primary-interop-assembly"></a>Microsoft Office InfoPath プライマリ相互運用機能アセンブリについて

InfoPath アプリケーションは COM (コンポーネント オブジェクト モデル) アプリケーションとして作成されており、外部オートメーションのプログラミング インターフェイスを COM インターフェイスとして公開します。 Visual C# や Visual Basic などのマネージ コード言語を使用する InfoPath ソリューションの作成をサポートするために、InfoPath セットアップ プログラムの **.NET** プログラミング サポート オプションは、3 つの相互運用機能アセンブリをインストールします。 相互運用アセンブリとは、マネージ コードとアンマネージ コードの仲介役として機能する .NET アセンブリで、COM オブジェクトのメンバーを、対応する .NET マネージ メンバーにマップします。 
  
InfoPath によってインストールされる 3 つの相互運用アセンブリのファイルを以下に示します。
  
- Microsoft.Office.Interop.InfoPath.dll
    
- Microsoft.Office.Interop.InfoPath.SemiTrust.dll
    
- Microsoft.Office.Interop.InfoPath.Xml.dll
    
このトピックでは、Microsoft.Office.Interop.InfoPath の相互運用機能アセンブリによって公開されるオブジェクト モデルについて説明します。これは、外部オートメーション コードでのみ使用されます。InfoPath フォーム テンプレート (.xsn) 内から実行するマネージ コードの作成と実行のためにのみ使用される Microsoft.Office.Interop.InfoPath.SemiTrust アセンブリの詳細については、「[InfoPath 2003 の互換性のあるオブジェクト モデル](https://msdn.microsoft.com/library/e4511af6-d7e7-44ad-a50d-1b7ee04f8215%28Office.15%29.aspx)」を参照してください。
  
## <a name="important-installation-information"></a>インストールに関する重要な情報

InfoPath セットアップ プログラムの既定のインストール オプションは、Microsoft をインストールします。Office.Interop.InfoPath アセンブリは、グローバル アセンブリ キャッシュ (GAC) で、その内容を C:\Windows\Assembly フォルダー (またはファイル システムを直接表示するときに C:\Windows\assembly\GAC_MSIL で表示できます)。 このアセンブリは、「Microsoft Office InfoPath プライマリ相互運用機能アセンブリ」と呼ばれますが、よく Microsoft.Office.Interop.InfoPath.Xml アセンブリと共に使用され、GAC にインストールされてマネージ コードを使用する外部アプリケーションから InfoPath アプリケーションを自動化します。 Microsoft.Office.Interop.InfoPath.Xml アセンブリの詳細については、「[InfoPath XML 相互運用機能アセンブリについて](about-the-infopath-xml-interop-assembly.md)」を参照してください。
  
Microsoft の場合。Office.Interop.InfoPath アセンブリが GAC に表示されない場合は、InfoPath が正しくインストールされていることを確認する必要があります。 既定で、セットアップ プログラムの **.NET プログラミング サポート** オプションは、セットアップを実行する前に、.NET Framework 1.1 再頒布可能パッケージ、.NET Framework 1.1 Software Development Kit (SDK)、またはそれ以降のバージョンの.NET Framework がインストールされている限り、**[マイ コンピューターから実行]** に設定されます。 これらの相互運用機能アセンブリがコンピューターで使用できない場合は、.NET Framework 1.1 以降がインストールされていることを確認してから、コントロール パネルの プログラムと機能を使用して、Microsoft Office InfoPath の **[.NET** プログラミングサポート]オプションを [マイ コンピューターから実行] に設定してセットアップを変更する必要があります。
  
1.1 再頒布可能.NET Frameworkダウンロードの詳細については、「.NET Framework [1.1 再頒布可能」を参照してください](https://www.microsoft.com/en-us/download/details.aspx?id=26)。
  
## <a name="the-microsoftofficeinteropinfopath-namespace"></a>Microsoft.Office.Interop.InfoPath 名前空間

特定のタスクのマネージ コードを作成するプロセスは、Visual Basic for Applications や JScript などの言語を使用して行う同じタスクと似ていますが、Microsoft Visual Studio の **オブジェクト ブラウザー** から **Microsoft.Office.Interop.InfoPath** 名前空間を表示するときに公開されるオブジェクト モデルはさらに複雑です。これは、.NET Framework の相互運用性は、すべての public インターフェイスを公開する COM サーバー、および .NET Framework 自体に必要ないくつかの追加の構成要素を必要とするためです。相互運用機能アセンブリによって公開されるオブジェクト モデルがどのように複雑に見えるか、またその理由の詳細については、「[InfoPath 2003 の互換性のあるオブジェクト モデル](../form-templates/infopath-2003-compatible-object-models.md)」のトピックの「COM オブジェクトが InfoPath 2003 互換オブジェクト モデルに公開されるしくみ」を参照してください。 
  
### <a name="using-intellisense"></a>IntelliSense を使用する

このセクションの例では、Microsoft への参照が確立されている必要があります。Office.Interop.InfoPath とMicrosoft.Office.Interop.InfoPath.Xmlアセンブリ。 参照と追加の外部オートメーションの例を設定する方法については、「外部オートメーションのシナリオと例 [」を参照してください](external-automation-scenarios-and-examples.md)。
  
外部オートメーション コードで Microsoft IntelliSense ステートメント補完を使用する前に、次のコード行に示すように[、Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Application.aspx)クラスのインスタンスのオブジェクト変数を作成する必要があります。 
  
```cs
Application myApp = 
    new Microsoft.Office.Interop.InfoPath.Application();
```

```vb
Dim myApp As Application = _
    New Microsoft.Office.Interop.InfoPath.Application()
```

オブジェクト変数を作成した後で、変数名に続けてピリオドを入力すると、**Application** クラスの選択できるメンバーのドロップダウン リストが表示されます。 
  
**InfoPath** フォームを使用するには [、XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.XDocument.aspx)型のオブジェクト変数を宣言し、次のコード行に示すように Application オブジェクト変数 [の XDocuments](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.XDocuments.aspx)コレクションからフォームを開いて初期化します。 
  
```cs
XDocument myXDoc = myApp.XDocuments.Open(
    "c:\\temp\\Form1.xml",
    (int) XdDocumentVersionMode.xdFailOnVersionOlder);
```

```vb
Dim myXDoc As XDocument = myApp.XDocuments.Open( _
    "c:\\temp\\Form1.xml", _
    XdDocumentVersionMode.xdFailOnVersionOlder)
```

変数の名前とその後のピリオドを入力すると、**XDocument** クラスのメンバーの IntelliSense ステートメント入力候補のドロップダウン リストが表示されます。 
  
Microsoft XML Core Services (MSXML) を使用してフォームの基になる XML ドキュメントの内容を操作するには [、IXMLDOMDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Xml.IXMLDOMDocument2.aspx)型の変数を作成し **、XDocument** クラスの [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._XDocument2.DOM.aspx)プロパティを使用して、フォームの XML ドキュメント オブジェクト モデル (DOM) をその変数に割り当てる必要があります。 
  
```cs
IXMLDOMDocument2 doc= myXDoc.DOM as IXMLDOMDocument2;
```

```vb
Dim doc As IXMLDOMDocument2 = myXDoc.DOM
```

変数の名前とその後のピリオドを入力すると、**IXMLDOMDocument2** クラスのメンバーの IntelliSense ステートメント入力候補のドロップダウン リストが表示されるので、MSXML を使用して XML ドキュメントを操作できます。 
  
### <a name="using-the-class-library-reference-documentation"></a>クラス ライブラリ リファレンス ドキュメントを使用する

[Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.aspx)名前空間クラス ライブラリリファレンス ドキュメントの組織は、コクラス インターフェイスと、実装する継承されたインターフェイスとの関係を反映しています。 
  
[Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Application.aspx)などのコクラス インターフェイスのトピックを開く場合、トピックの先頭にあるインターフェイスの説明に続くコクラス インターフェイスのメンバーへのリンクには、空のトピックが表示されます。 コクラス インターフェイスによって実装されるメンバーの一覧を表示するには、そのコクラスによって継承される最も新しいインターフェイスのトピックを開き、そのメンバーの表を開く必要があります。 継承インターフェイスへのリンクは、コクラス インターフェイスのトピックの「解説」セクションの先頭にあります。 
  
Visual Studio コード エディターで F1 キーを押した場合の動作は、大抵の場合インターフェイスのメンバーを操作しているので、F1 ヘルプを呼び出したメンバーが直接表示されることを除いては、ほぼ同様です。 ただし、メンバーがバージョン付きのインターフェイスから実装される場合があるという点で、初めは混乱する可能性があります。 たとえば、「 `myXDocument.UI.Alert`」と入力し、 `Alert` にカーソルを置いて F1 キーを押すと、「UI2.Alert メソッド」というタイトルのトピックが表示されます。 これは、 **Alert** メソッドが **UI2** インターフェイスのメンバーの実装であるからです。 
  
### <a name="passing-optional-parameters-to-infopath-object-model-members"></a>InfoPath オブジェクト モデルのメンバーにオプションのパラメーターを渡す

InfoPath オブジェクト モデルのメンバーにオプションのパラメーターが含まれており、さらにそのパラメーターの値を指定しない場合は、そのパラメーターの代わりに **Type.Missing** フィールドを渡す必要があります。 実際の値を省略する場合に **Type.Missing** フィールドを渡さないと、ビルド エラーが発生します。 これは、C# と Visual Basic のどちらで書かれたコードにも当てはまります。 たとえば、 [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.View2.SelectNodes.aspx) インターフェイスの [SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ViewObject.aspx) メソッドには、  _varEndNode_ と  _varViewContext_ という 2 つのオプション パラメーターが含まれています。 これらのオプション パラメーターに対して実際の値を指定しないコード行は、次のようになっている必要があります。
  
```cs
myXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing);
```

```vb
myXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing)
```

## <a name="see-also"></a>関連項目

- [外部自動化のシナリオと例](external-automation-scenarios-and-examples.md)

