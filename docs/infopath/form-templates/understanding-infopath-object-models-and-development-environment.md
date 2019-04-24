---
title: InfoPath のオブジェクト モデルと開発環境を理解する
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- infopath 2007, object models,object models [InfoPath 2007],InfoPath 2007, development environments
localization_priority: Normal
ms.assetid: 29415c5b-9a42-46f4-a9e8-6a7d5bb7bdbf
description: Microsoft InfoPath 2013 は、フォーム テンプレートでのビジネス ロジック開発用に 2 種類のプログラミング モデルをサポートしており、マネージ コードからの外部自動化もサポートしています。
ms.openlocfilehash: c2ed1254acf86136ab7144c732aef91ac4c14c53
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303459"
---
# <a name="understanding-infopath-object-models-and-development-environment"></a>InfoPath のオブジェクト モデルと開発環境を理解する

Microsoft InfoPath 2013 は、フォーム テンプレートでのビジネス ロジック開発用に 2 種類のプログラミング モデルをサポートしており、マネージ コードからの外部自動化もサポートしています。
  
SharePoint Server 2013 で利用できる InfoPath Forms Services を使用すると、Web ブラウザーで InfoPath フォームに入力できるようになります。InfoPath Forms Services を実行しているサーバーに、ブラウザー互換フォーム テンプレートに基づくフォーム (.xsn) を展開すると、コンピューターに InfoPath がインストールされていなくても Web ブラウザーでフォームを開くことができます。InfoPath がインストールされている場合は、InfoPath でフォームが開きます。InfoPath Forms Services は、InfoPath フォーム テンプレートの発行と管理に関連するサーバー タスクを自動化するためのオブジェクト モデルも提供します。
  
InfoPath 2013 は、Visual Studio 2012 プログラミング環境および関連付けられたプログラミング言語をサポートしています (このトピックで後述します)。
  
## <a name="infopath-programming-models"></a>InfoPath のプログラミング モデル

InfoPath 2013 は、フォーム テンプレートでのビジネス ロジック開発用に、次の 2 種類のオブジェクト モデルをサポートしています。
  
- InfoPath のマネージ コード オブジェクト モデル
    
- InfoPath 2003 互換のマネージ コード オブジェクト モデル
    
また、InfoPath 2013 では、外部アプリケーションから InfoPath を自動化するためのマネージ コードを記述することもできます。
  
InfoPath Forms Services は、サーバー タスクを自動化するためのオブジェクト モデルを提供します。このようなタスクには、サーバー管理者のアクセス許可が必要となる、サーバー上で実行されているコードからのフォーム テンプレートの検証とアップロードなどが含まれます。
  
> [!NOTE]
> InfoPath Filler 2013 では、スクリプト言語 (JScript および VBScript) で記述されたビジネス ロジックを使用する、以前のバージョンの InfoPath で作成された InfoPath フォーム テンプレート ソリューションを開いて実行できます。ただし、InfoPath Designer 2010 では、スクリプトで記述されたビジネス ロジックを使用するフォーム テンプレートの作成または変更をサポートしていません。 
  
### <a name="the-infopath-managed-code-object-model"></a>InfoPath のマネージ コード オブジェクト モデル

InfoPath 2013 マネージ コード オブジェクト モデルは 2 つのアセンブリで実装されており、どちらも Microsoft.Office.Infopath.dll という名前です。
  
一方のバージョンのアセンブリには、InfoPath Forms Services を実行する SharePoint Server 2013 で動作する、ブラウザー対応のフォーム テンプレートとして展開されたフォーム テンプレートのビジネス ロジックでサポートされている型とメンバーのみを含む、InfoPath オブジェクト モデルのサブセットが実装されています。このアセンブリに対して記述されたビジネス ロジックを使用するフォーム テンプレートは、InfoPath Filler および Web ブラウザーで開いて実行できます。
  
もう 1 つのバージョンのアセンブリには、ブラウザー対応のフォーム テンプレートのビジネス ロジックでサポートされていない機能を提供する追加の型とメンバーが実装されています。このアセンブリ内で追加のクラスとメンバーに対して書かれたビジネス ロジックを含むフォーム テンプレートは、InfoPath Filler のエディターでのみ開き、実行することができます。
  
> [!NOTE]
> フォーム テンプレートが InfoPath Filler または Web ブラウザーのどちらの環境で実行されるかを指定するために、[Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) クラスのプロパティを使用する条件付きロジックを書くことができます。 この条件付きロジックを使用して、ビジネス ロジックを、Web ブラウザーで動作するコードと、InfoPath Filler のエディターでのみ動作するクラスおよびメンバーに対して書かれたコードの間で分岐することができます。 詳細については、「[実行時の環境を指定する条件付きロジックを書く方法](how-to-write-conditional-logic-that-determines-the-run-time-environment.md)」を参照してください。
  
InfoPath Designer で新しいフォームの設計を開始する際に Microsoft Office Backstage の [ **新規作成**] タブで [ **空白のフォーム**] または [ **空白のフォーム (InfoPath Filler)**] フォーム テンプレートのどちらを選択するかによって、フォーム テンプレートのためのビジネス ロジックの追加およびコンパイルの際に InfoPath で使用されるアセンブリは異なります。[ **空白のフォーム**] フォーム テンプレートを使用して作成されたフォームは、ブラウザー対応のフォーム テンプレートとして展開されたフォーム テンプレートのビジネス ロジックでサポートされている型とメンバーのみを含むアセンブリを使用します。[ **空白のフォーム**] フォーム テンプレートを使用して作成されたフォームは、Web ブラウザーおよび InfoPath Filler の両方で開くことができます。[ **空白のフォーム (InfoPath Filler)**] フォーム テンプレートを使用して作成されたフォームは、ブラウザー対応のフォーム テンプレートのビジネス ロジックでサポートされていない機能を提供する追加の型とメンバーが実装されているアセンブリを使用し、InfoPath Filler でのみ開くことができます。 
  
> [!TIP]
> フォーム テンプレートのデザインを開始した後で、フォームの互換性設定を変更することによって、使用するアセンブリを変更できます。そのためには、[ **開発**] タブで [ **言語**] をクリックし、[ **カテゴリ**] リストで [ **互換性**] をクリックします。SharePoint Server 2013 にブラウザー互換フォームとして展開できるフォームを作成する場合は、[ **フォームの種類**] リストで [ **Web ブラウザー フォーム**] を選択します。InfoPath Filler のエディターでのみ実行できるフォームを作成する場合は、[ **InfoPath Filler フォーム**] を選択します。[ **フォームの種類**] リストの他のオプションは、InfoPath 2007 および InfoPath 2003 との互換性をサポートしています。 
  
この両バージョンのオブジェクト モデルのクラスとメンバーは、[Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) 名前空間で公開されています。これらのアセンブリは、InfoPath 2013 インストールの次のディレクトリにあります。 
  
|**アセンブリ**|**説明**|
|:-----|:-----|
|Microsoft.Office.InfoPath.dll           (C:\Program Files\Microsoft Office\Office15\InfoPathOM\InfoPathOMFormServices ディレクトリ)  <br/> |InfoPath Forms Services を実行しているサーバーに展開されるフォーム テンプレートのビジネス ロジックで実行される型とメンバーのみを含むオブジェクト モデルのサブセット。  <br/> |
|Microsoft.Office.InfoPath.dll           (C:\Program Files\Microsoft Office\Office15\InfoPathOM ディレクトリ)  <br/> |InfoPath Forms Services に展開されるフォーム テンプレートのビジネス ロジックで実行されない型とメンバーも含む "完全な" オブジェクト モデル。  <br/> |
   
> [!NOTE]
> 上記で参照されるアセンブリは、コードの作成とコンパイルを行う設計時に使用されます。実行時に、フォーム テンプレートが InfoPath 内で開かれるときに使用されるアセンブリは、InfoPath がインストールされているコンピューターのグローバル アセンブリ キャッシュ (GAC) にあります。InfoPath Forms Services を実行しているサーバーから Web ブラウザー内でフォーム テンプレートが開かれるときは、使用されるアセンブリはサーバーにあります。 
  
2 つのアセンブリがあることで、ビジネス ロジックに、サポートされるフォーム エディター (Web ブラウザーまたは InfoPath Filler) に適したオブジェクト モデル メンバーへの呼び出しのみが含まれることが保証されます。たとえば、コードを編集する際、ステートメント入力候補やインライン ドキュメントなどの IntelliSense 機能は、対象となるフォーム エディターの適切なオブジェクト モデル メンバーに対してのみ表示および動作します。
  
Microsoft.Office.InfoPath アセンブリによって公開されるマネージ コード オブジェクト モデルのどちらのバージョンでも、ビジネス ロジック内での XML データ ストアのナビゲーションと更新には、 **System.Xml.XPath.XPathNavigator** クラスのメンバーへの呼び出しが必要です。InfoPath 2003 での XML データ ストアのナビゲーションと更新には、JScript または VBScript を使用して作成したビジネス ロジックの場合は MSXML クラスのメンバーの呼び出しが必要となり、C# または Visual Basic と Microsoft Office InfoPath 2003 Toolkit for Visual Studio .NET を使用して作成したビジネス ロジックの場合は **Microsoft.Office.Interop.InfoPath.SemiTrust** 名前空間によって提供される MSXML クラスのラッパーをとおした呼び出しが必要となります。 
  
**XPathNavigator** クラスのメンバーを使用すると、InfoPath クライアントで開くフォーム テンプレートと、Web 対応のフォーム (Web ブラウザーで InfoPath Forms Services を実行する SharePoint Server 2013 から開くフォーム) で開くフォーム テンプレートの DOM 操作を、同じビジネス ロジック コードでサポートできます。 
  
InfoPath マネージ コード フォーム テンプレートのビジネス ロジックでの **XPathNavigator** クラスのメンバーを操作する方法の詳細については、「[XPathNavigator クラスおよび XPathNodeIterator クラスを操作する方法](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md)」を参照してください。
  
### <a name="the-infopath-2003-compatible-managed-code-object-model"></a>InfoPath 2003 互換のマネージ コード オブジェクト モデル

InfoPath 2003 互換のマネージ コード オブジェクト モデルは、マネージ コードを使用してフォーム テンプレートでビジネス ロジックを記述するために、Microsoft Office InfoPath 2003 Toolkit for Visual Studio .NET と共に InfoPath 2003 Service Pack 1 で導入されました。このオブジェクト モデルは、InfoPath 2003 との互換性を維持するために、InfoPath 2013 でも引き続きサポートされています。
  
このオブジェクト モデルのクラスとメンバーは、[Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) 名前空間で公開されています。このオブジェクト モデルは、C:\Program Files\Microsoft Office\Office14 フォルダーにある次のアセンブリ ファイルに実装されています。 
  
|**アセンブリ**|**説明**|
|:-----|:-----|
|Microsoft.Office.Interop.InfoPath.SemiTrust.dll  <br/> |C# または Visual Basic .NET を使用して書かれたフォーム テンプレート ビジネス ロジックのための、InfoPath COM オブジェクト モデルに対する COM 相互運用機能を提供します。  <br/> |
   
> [!NOTE]
> Microsoft.Office.Interop.InfoPath.SemiTrust アセンブリによって提供される COM 相互運用マネージ コード オブジェクト モデルを使用したビジネス ロジックの作成は InfoPath 2013 で引き続きサポートされていますが、このオブジェクト モデルを使用して記述されたビジネス ロジックは、InfoPath Forms Services を実行する SharePoint Server 2013 に展開されたブラウザー対応のフォーム テンプレートではサポートされていません。ブラウザー対応のフォーム テンプレートでは、カスタム ビジネス ロジックに InfoPath マネージ コード オブジェクト モデルを使用する必要があります。 
  
### <a name="automating-infopath-from-managed-code"></a>マネージ コードから InfoPath を自動化する

マネージ コードを使用したビジネス ロジックの作成に加え、開発者は外部アプリケーションで実行されるマネージ コードを使用して InfoPath を自動化することもできます。この機能と、コードを記述するために必要なアセンブリは、InfoPath 2003 Service Pack 1 で導入されました。InfoPath の自動化に使用するオブジェクトとメンバーは、InfoPath 2013 の外部自動化コードを記述する際の追加機能を提供するために更新されました。
  
外部自動化に使用するクラスとメンバーは、 [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) 名前空間と [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml) 名前空間で公開されています。自動化コードを記述するために必要なアセンブリ ファイルは、C:\Program Files\Microsoft Office\Office14 フォルダーにあります。 
  
|**アセンブリ**|**説明**|
|:-----|:-----|
|Microsoft.Office.Interop.InfoPath.dll  <br/> |C# または Visual Basic を使用して書かれた外部自動化コードのための、InfoPath COM オブジェクト モデルに対する COM 相互運用機能を提供します。  <br/> |
|Microsoft.Office.Interop.InfoPath.Xml.dll  <br/> |C# または Visual Basic を使用して記述された外部自動化コードのための、MSXML for XML DOM 操作に対する COM 相互運用機能を提供します。  <br/> |
   
外部アプリケーションからマネージ コードを使用して InfoPath アプリケーションを自動化するためだけに使用される、 **Microsoft.Office.Interop.InfoPath** 名前空間と **Microsoft.Office.Interop.InfoPath.Xml** 名前空間で提供されるオブジェクト モデルの詳細については、 [InfoPath デベロッパー ポータル](https://msdn.microsoft.com/office/aa905434.aspx)を参照してください。
  
### <a name="the-infopath-forms-services-object-model"></a>InfoPath Forms Services オブジェクト モデル

InfoPath Forms Services の管理タスクを自動化するマネージ コード オブジェクト モデルは、Microsoft SharePoint Server 2013 インストールの \<ドライブ\>:\Program Files\Microsoft Office Server\15.0\Bin にある Microsoft.Office.InfoPath.Server.dll に実装されています。
  
|**アセンブリ**|**説明**|
|:-----|:-----|
|Microsoft.Office.InfoPath.Server.dll  <br/> |ブラウザー対応のフォーム テンプレートを読み込んだり、アクティブ化、非アクティブ化するなどの InfoPath Forms Services タスクを自動化するオブジェクト モデル。  <br/> |
   
InfoPath Forms Services オブジェクト モデルの詳細については、MSDN で提供される SharePoint Server 2013 ソフトウェア開発キット (SDK) を参照してください。
  
## <a name="infopath-development-environment"></a>InfoPath 開発環境

InfoPath 2013 フォーム テンプレートでのビジネス ロジックの開発は、[Microsoft Visual Studio Tools for Applications 2012](https://www.microsoft.com/en-us/download/details.aspx?id=38807) アドオンがインストールされた Visual Studio 2012 を使用して行うことができます。 
  
> [!NOTE]
> InfoPath 2013 は、JScript または VBScript で記述されたビジネス ロジックを使用するフォーム テンプレートの作成や編集をサポートしていませんが、InfoPath Filler では、以前のバージョンの InfoPath で作成されたスクリプト ベースのフォーム テンプレートを開くことができます。 
  
## <a name="see-also"></a>関連項目

- [チュートリアル: コードを含む基本的なフォーム テンプレートの作成](walkthrough-creating-a-basic-form-template-with-code.md)
- [[ウォークスルー] InfoPath 2003 オブジェクト モデルを使用して基本的なフォーム テンプレートを作成およびデバッグする方法](walkthrough-create-and-debug-basic-form-template-using-infopath-object-model.md)

