---
title: Microsoft Office InfoPath プライマリ相互運用機能アセンブリについて
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2007 では、プライマリ相互運用機能アセンブリでは、InfoPath プライマリ相互運用機能アセンブリ、Pia の [InfoPath 2007] では、プライマリ相互運用機能アセンブリを [InfoPath 2007]
localization_priority: Normal
ms.assetid: 1b3ae03c-6951-49e4-a489-4712d3f7ba72
description: Visual C# や Visual Basic などのマネージ コード言語を使用して InfoPath ソリューションの作成をサポートするには、InfoPath セットアップ プログラムで [.NET プログラミング サポート] オプションは、次の 3 つの相互運用機能アセンブリをインストールします。
ms.openlocfilehash: b6b37254773d758dc064e22045d68f29febe7bbe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799012"
---
# <a name="about-the-microsoft-office-infopath-primary-interop-assembly"></a>Microsoft Office InfoPath プライマリ相互運用機能アセンブリについて

InfoPath アプリケーションの COM インターフェイスと外部の自動化のためのプログラミング インターフェイスを公開するコンポーネント オブジェクト モデル (COM) アプリケーションとしてビルドします。 Visual C# や Visual Basic などのマネージ コード言語を使用して InfoPath ソリューションの作成をサポートするには、InfoPath セットアップ プログラムで [ **.NET プログラミング サポート**] オプションは、次の 3 つの相互運用機能アセンブリをインストールします。 相互運用アセンブリとは、マネージ コードとアンマネージ コードの仲介役として機能する .NET アセンブリで、COM オブジェクトのメンバーを、対応する .NET マネージ メンバーにマップします。 
  
InfoPath によってインストールされる 3 つの相互運用アセンブリのファイルを以下に示します。
  
- Microsoft.Office.Interop.InfoPath.dll
    
- Microsoft.Office.Interop.InfoPath.SemiTrust.dll
    
- Microsoft.Office.Interop.InfoPath.Xml.dll
    
このトピックでは、専用外部オートメーション コードの使用は、Microsoft.Office.Interop.InfoPath の相互運用機能アセンブリによって公開されるオブジェクト モデルについて説明します。 Microsoft.Office.Interop.InfoPath.SemiTrust アセンブリを記述し、InfoPath フォーム テンプレート (.xsn) 内から実行するマネージ コードを実行するためだけに使用する方法については、 [InfoPath 2003 の互換性のあるオブジェクト モデル](http://msdn.microsoft.com/library/e4511af6-d7e7-44ad-a50d-1b7ee04f8215%28Office.15%29.aspx)を参照してください。
  
## <a name="important-installation-information"></a>インストールに関する重要な情報

InfoPath セットアップ プログラムの既定のインストール オプションは、Microsoft.Office.Interop.InfoPath アセンブリで、グローバル アセンブリ キャッシュ (GAC)、C:\Windows\Assembly フォルダー (または C:\Windows\assembly\GAC_ で、先の内容を表示できますをインストールします。MSIL ファイル ・ システムを直接表示する場合)。 このアセンブリは、「Microsoft Office InfoPath プライマリ相互運用機能アセンブリ」と呼ばれますは、Microsoft.Office.Interop.InfoPath.Xml アセンブリを GAC にインストールされてと組み合わせてから InfoPath アプリケーションを自動化するにはマネージ コードを使用する外部のアプリケーションです。 Microsoft.Office.Interop.InfoPath.Xml アセンブリの詳細については、 [InfoPath の XML の相互運用機能アセンブリの詳細](about-the-infopath-xml-interop-assembly.md)を参照してください。
  
Microsoft.Office.Interop.InfoPath アセンブリが GAC に表示されない場合は、InfoPath が正しくインストールされていることを確認する必要があります。 **マイ コンピューターから実行**まで、.NET Framework 1.1 再配布可能な.NET Framework 1.1 ソフトウェア開発キット (SDK)、またはそれ以降のバージョンの.NET Framework のセットアップ プログラムで [ **.NET プログラミング サポート**] オプションを設定する既定では、セットアップを実行する前にインストールされています。 これらの相互運用機能アセンブリがコンピューターで利用できない場合は、1.1 以降の.NET Framework がインストールされていると **.NET のプログラミング機能を設定することにより設定を変更するのには**プログラムと機能**、[**コントロール パネル**] からを使用しているを確認する必要があります。サポート**[ **Microsoft Office InfoPath**で **[マイ コンピューターから実行**する] オプション。
  
.NET Framework 1.1 再配布可能なダウンロードについては、 [.NET Framework 1.1 再配布可能な](http://msdn.microsoft.com/netframework/technologyinfo/redist/default.aspx)を参照してください。
  
## <a name="the-microsoftofficeinteropinfopath-namespace"></a>Microsoft.Office.Interop.InfoPath 名前空間

所定のタスク用のコードがまたは JScript では、 **Microsoft.Office.Interop.InfoPath**を表示するときに公開されるオブジェクト モデルの Visual Basic for Applications などの言語を使用して同じタスクを実行することに非常に類似したドキュメントの作成プロセスの管理Microsoft Visual Studio の**オブジェクト ブラウザー**からの名前空間より複雑な検索します。 これは、.NET Framework の相互運用性と、.NET Framework 自体に必要ないくつか追加の構成要素を使用して、すべてのパブリック インターフェイスを公開する COM サーバーを必要とするためです。 相互運用機能アセンブリによって公開されるオブジェクト モデルがより複雑な表示方法とその理由の詳細については、 [InfoPath 2003 の互換性のあるオブジェクト モデル](http://msdn.microsoft.com/library/e4511af6-d7e7-44ad-a50d-1b7ee04f8215%28Office.15%29.aspx)のトピックの「方法 COM オブジェクトが公開するマネージ コード」セクションを参照してください。 
  
### <a name="using-intellisense"></a>IntelliSense を使用する

このセクションの例では、Microsoft.Office.Interop.InfoPath と Microsoft.Office.Interop.InfoPath.Xml のアセンブリへの参照を確立したことを前提としています。 参照とその他の外部オートメーションの例を設定する方法については、[外部オートメーションのシナリオと例](external-automation-scenarios-and-examples.md)を参照してください。
  
外部オートメーション コードでは、Microsoft IntelliSense のステートメント入力候補を使用できますが、前に、次のコード行に示すように[アプリケーション](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Application.aspx)クラスのインスタンスをオブジェクト変数を作成する必要があります。 
  
```cs
Application myApp = 
    new Microsoft.Office.Interop.InfoPath.Application();
```

```vb
Dim myApp As Application = _
    New Microsoft.Office.Interop.InfoPath.Application()
```

オブジェクト変数を作成した後には、変数名に続けて、ピリオドを入力するとき] ボックスの一覧が表示されますを選択するのには、**アプリケーション**クラスのメンバー。 
  
InfoPath フォームを操作するには、 [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.XDocument.aspx)の型のオブジェクト変数を宣言し、 [XDocuments](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.XDocuments.aspx)コレクションの次のコード行に示すように**アプリケーション**オブジェクトの変数からフォームを開くことで初期化します。 
  
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

**XDocument**クラスのメンバーの IntelliSense のステートメント入力候補のドロップダウン ・ リストは、ピリオドの後に変数の名前を入力するときに表示されます。 
  
Microsoft XML Core Services (MSXML) を使用して、フォームの基になる XML ドキュメントの内容を操作するには必要があります[IXMLDOMDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Xml.IXMLDOMDocument2.aspx)の型の変数を作成し、XML を割り当てるには、 **XDocument**クラスの[DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._XDocument2.DOM.aspx)プロパティを使用してドキュメント オブジェクト モデル (DOM) その変数をフォームのです。 
  
```cs
IXMLDOMDocument2 doc= myXDoc.DOM as IXMLDOMDocument2;
```

```vb
Dim doc As IXMLDOMDocument2 = myXDoc.DOM
```

使用すると、MSXML を使用して、XML ドキュメントで作業するのには、ピリオドの後に変数の名前を入力するときは、 **IXMLDOMDocument2**クラスのメンバーの IntelliSense のステートメント入力候補のドロップダウン リストが表示されます。 
  
### <a name="using-the-class-library-reference-documentation"></a>クラス ライブラリ リファレンス ドキュメントを使用する

[Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.aspx)名前空間のクラス ライブラリのリファレンス ドキュメントの組織では、コクラスのインターフェイスと実装、継承されたインターフェイスとの間の関係が反映されます。 
  
[アプリケーション](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Application.aspx)など、コクラスのインターフェイスのトピックを開くと、トピックの先頭にインターフェイスの説明に続くコクラス インターフェイスのメンバーへのリンクには、空のトピックが表示されます。 コクラス インターフェイスによって実装されるメンバーの一覧を表示するには、そのコクラスによって継承される最も新しいインターフェイスのトピックを開き、そのメンバーの表を開く必要があります。 継承インターフェイスへのリンクは、コクラス インターフェイスのトピックの「解説」セクションの先頭にあります。 
  
Visual Studio コード エディターで f1 キーを押して、動作と同様に、F1 ヘルプを起動するにメンバーが直接表示されます最も通常、インターフェイスのメンバーを使用しているためです。 ただし、メンバーがバージョン付きのインターフェイスから実装される場合があるという点で、初めは混乱する可能性があります。 たとえば、「 `myXDocument.UI.Alert`」と入力し、 `Alert` にカーソルを置いて F1 キーを押すと、「UI2.Alert メソッド」というタイトルのトピックが表示されます。 これは、 **Alert** メソッドが **UI2** インターフェイスのメンバーの実装であるからです。 
  
### <a name="passing-optional-parameters-to-infopath-object-model-members"></a>InfoPath オブジェクト モデルのメンバーにオプションのパラメーターを渡す

InfoPath オブジェクト モデル メンバーには、オプションのパラメーターが含まれていて、そのパラメーターの値を指定しない場合は、そのパラメーターの**Type.Missing**フィールドを渡す必要があります。 実際の値を省略する場合に **Type.Missing** フィールドを渡さないと、ビルド エラーが発生します。 これは、C# と Visual Basic の両方で記述されたコードの場合は true。 たとえば、 [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.View2.SelectNodes.aspx) インターフェイスの [SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ViewObject.aspx) メソッドには、  _varEndNode_ と  _varViewContext_ という 2 つのオプション パラメーターが含まれています。 これらのオプション パラメーターに対して実際の値を指定しないコード行は、次のようになっている必要があります。
  
```cs
myXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing);
```

```vb
myXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing)
```

## <a name="see-also"></a>関連項目

- [外部オートメーションのシナリオと例](external-automation-scenarios-and-examples.md)

