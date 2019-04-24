---
title: Microsoft Office InfoPath プライマリ相互運用機能アセンブリについて
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2007、プライマリ相互運用機能アセンブリ、infopath プライマリ相互運用機能アセンブリ、pia [infopath 2007]、プライマリ相互運用機能アセンブリ [infopath 2007]
localization_priority: Normal
ms.assetid: 1b3ae03c-6951-49e4-a489-4712d3f7ba72
description: visual C# や visual Basic などのマネージコード言語を使用する infopath ソリューションの作成をサポートするために、infopath セットアッププログラムの .net プログラミングサポートオプションは3つの相互運用機能アセンブリをインストールします。
ms.openlocfilehash: 51773ad46b1371c410c4249e13a489f0c5550cd1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310137"
---
# <a name="about-the-microsoft-office-infopath-primary-interop-assembly"></a><span data-ttu-id="f9380-104">Microsoft Office InfoPath プライマリ相互運用機能アセンブリについて</span><span class="sxs-lookup"><span data-stu-id="f9380-104">About the Microsoft Office InfoPath Primary Interop Assembly</span></span>

<span data-ttu-id="f9380-105">InfoPath アプリケーションは COM (コンポーネント オブジェクト モデル) アプリケーションとして作成されており、外部オートメーションのプログラミング インターフェイスを COM インターフェイスとして公開します。</span><span class="sxs-lookup"><span data-stu-id="f9380-105">The InfoPath application is built as a Component Object Model (COM) application that exposes its programmability interfaces for external automation as COM interfaces.</span></span> <span data-ttu-id="f9380-106">visual C# や visual Basic などのマネージコード言語を使用する infopath ソリューションの作成をサポートするために、infopath セットアッププログラムの **.net プログラミングサポート**オプションは3つの相互運用機能アセンブリをインストールします。</span><span class="sxs-lookup"><span data-stu-id="f9380-106">To support the creation of InfoPath solutions that use managed-code languages such as Visual C# and Visual Basic, the **.NET Programmability Support** option in the InfoPath setup program installs three interop assemblies.</span></span> <span data-ttu-id="f9380-107">相互運用アセンブリとは、マネージ コードとアンマネージ コードの仲介役として機能する .NET アセンブリで、COM オブジェクトのメンバーを、対応する .NET マネージ メンバーにマップします。</span><span class="sxs-lookup"><span data-stu-id="f9380-107">Interop assemblies are .NET assemblies that act as a bridge between managed and unmanaged code, mapping COM object members to equivalent .NET managed members.</span></span> 
  
<span data-ttu-id="f9380-108">InfoPath によってインストールされる 3 つの相互運用アセンブリのファイルを以下に示します。</span><span class="sxs-lookup"><span data-stu-id="f9380-108">The files for the three interop assemblies installed by InfoPath are named:</span></span>
  
- <span data-ttu-id="f9380-109">Microsoft.Office.Interop.InfoPath.dll</span><span class="sxs-lookup"><span data-stu-id="f9380-109">Microsoft.Office.Interop.InfoPath.dll</span></span>
    
- <span data-ttu-id="f9380-110">Microsoft.Office.Interop.InfoPath.SemiTrust.dll</span><span class="sxs-lookup"><span data-stu-id="f9380-110">Microsoft.Office.Interop.InfoPath.SemiTrust.dll</span></span>
    
- <span data-ttu-id="f9380-111">Microsoft.Office.Interop.InfoPath.Xml.dll</span><span class="sxs-lookup"><span data-stu-id="f9380-111">Microsoft.Office.Interop.InfoPath.Xml.dll</span></span>
    
<span data-ttu-id="f9380-112">このトピックでは、外部オートメーションコードに対してのみ使用されるオブジェクトモデルについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f9380-112">This topic discusses the object model exposed through the Microsoft.Office.Interop.InfoPath interop assembly, which is used exclusively for external automation code.</span></span> <span data-ttu-id="f9380-113">SemiTrust アセンブリの詳細については、「infopath のフォームテンプレート (.xsn)」で実行されるマネージコードを記述して実行するためにのみ使用されます。「 [infopath 2003 互換オブジェクトモデル](https://msdn.microsoft.com/library/e4511af6-d7e7-44ad-a50d-1b7ee04f8215%28Office.15%29.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f9380-113">For information on the Microsoft.Office.Interop.InfoPath.SemiTrust assembly, which is used exclusively for writing and running managed code that runs from within InfoPath form templates (.xsn), see [InfoPath 2003 Compatible Object Models](https://msdn.microsoft.com/library/e4511af6-d7e7-44ad-a50d-1b7ee04f8215%28Office.15%29.aspx).</span></span>
  
## <a name="important-installation-information"></a><span data-ttu-id="f9380-114">インストールに関する重要な情報</span><span class="sxs-lookup"><span data-stu-id="f9380-114">Important Installation Information</span></span>

<span data-ttu-id="f9380-115">infopath セットアッププログラムの既定のインストールオプションでは、グローバルアセンブリキャッシュ (GAC) に C:\Windows\Assembly アセンブリがインストールされます。その内容は、フォルダー (または C:\Windows\assembly\GAC_) から表示できます。ファイルシステムを直接表示するときの MSIL)。</span><span class="sxs-lookup"><span data-stu-id="f9380-115">The default installation option of the InfoPath setup program installs the Microsoft.Office.Interop.InfoPath assembly in the Global Assembly Cache (GAC), the contents of which can be viewed from the C:\Windows\Assembly folder (or in C:\Windows\assembly\GAC_MSIL when viewing the file system directly).</span></span> <span data-ttu-id="f9380-116">このアセンブリは、「Microsoft Office InfoPath プライマリ相互運用機能アセンブリ」と呼ばれますが、よく Microsoft.Office.Interop.InfoPath.Xml アセンブリと共に使用され、GAC にインストールされてマネージ コードを使用する外部アプリケーションから InfoPath アプリケーションを自動化します。</span><span class="sxs-lookup"><span data-stu-id="f9380-116">This assembly is referred to as the "Microsoft Office InfoPath Primary Interop Assembly" and is often used in conjunction with the Microsoft.Office.Interop.InfoPath.Xml assembly, which is also installed in the GAC, to automate the InfoPath application from external applications that use managed code.</span></span> <span data-ttu-id="f9380-117">Microsoft.Office.Interop.InfoPath.Xml アセンブリの詳細については、「[InfoPath XML 相互運用機能アセンブリについて](about-the-infopath-xml-interop-assembly.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f9380-117">For information about the Microsoft.Office.Interop.InfoPath.Xml assembly, see [About the InfoPath XML Interop Assembly](about-the-infopath-xml-interop-assembly.md).</span></span>
  
<span data-ttu-id="f9380-118">GAC に、infopath アセンブリが表示されていない場合は、infopath が正しくインストールされていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9380-118">If the Microsoft.Office.Interop.InfoPath assembly is not visible in the GAC, you should confirm that InfoPath was installed correctly.</span></span> <span data-ttu-id="f9380-119">既定で、セットアップ プログラムの **.NET プログラミング サポート** オプションは、セットアップを実行する前に、.NET Framework 1.1 再頒布可能パッケージ、.NET Framework 1.1 Software Development Kit (SDK)、またはそれ以降のバージョンの.NET Framework がインストールされている限り、**[マイ コンピューターから実行]** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="f9380-119">By default, the **.NET Programmability Support** option in the setup program is set to **Run from My Computer** as long as the .NET Framework 1.1 Redistributable, .NET Framework 1.1 Software Development Kit (SDK), or a later version of the .NET Framework is installed before running setup.</span></span> <span data-ttu-id="f9380-120">これらの相互運用機能アセンブリがコンピューターで使用できない場合は、.net Framework 1.1 以降がインストールされていることを確認してから、**コントロールパネル**の [**プログラムと機能**] を使用して、 **.net プログラミングを設定してセットアップを変更する必要があります。** **Microsoft Office InfoPath**のサポートオプションで、 **[マイコンピューターから実行**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="f9380-120">If these interop assemblies are not available on your computer, you must confirm that .NET Framework 1.1 or later is installed, and then use **Programs and Features** from the **Control Panel** to change setup by setting the **.NET Programmability Support** option under **Microsoft Office InfoPath** to **Run from My Computer**.</span></span>
  
<span data-ttu-id="f9380-121">.net framework 1.1 再頒布可能パッケージのダウンロードについては、「 [.net framework 1.1 の再頒布可能](https://www.microsoft.com/en-us/download/details.aspx?id=26)パッケージ」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f9380-121">For information about downloading the .NET Framework 1.1 Redistributable, see [.NET Framework 1.1 Redistributable](https://www.microsoft.com/en-us/download/details.aspx?id=26).</span></span>
  
## <a name="the-microsoftofficeinteropinfopath-namespace"></a><span data-ttu-id="f9380-122">Microsoft.Office.Interop.InfoPath 名前空間</span><span class="sxs-lookup"><span data-stu-id="f9380-122">The Microsoft.Office.Interop.InfoPath Namespace</span></span>

<span data-ttu-id="f9380-123">特定のタスクのマネージ コードを作成するプロセスは、Visual Basic for Applications や JScript などの言語を使用して行う同じタスクと似ていますが、Microsoft Visual Studio の**オブジェクト ブラウザー**から **Microsoft.Office.Interop.InfoPath** 名前空間を表示するときに公開されるオブジェクト モデルはさらに複雑です。</span><span class="sxs-lookup"><span data-stu-id="f9380-123">Although the process of writing managed code for a given task is very similar to performing the same task using a language such as Visual Basic for Applications or JScript, the object model exposed when viewing the **Microsoft.Office.Interop.InfoPath** namespace from the **Object Browser** in Microsoft Visual Studio looks more complex.</span></span> <span data-ttu-id="f9380-124">これは、.NET Framework の相互運用性は、すべての public インターフェイスを公開する COM サーバー、および .NET Framework 自体に必要ないくつかの追加の構成要素を必要とするためです。</span><span class="sxs-lookup"><span data-stu-id="f9380-124">This is because interoperability with the .NET Framework requires a COM server to expose all of its public interfaces, as well as some additional constructs required by the .NET Framework itself.</span></span> <span data-ttu-id="f9380-125">相互運用機能アセンブリによって公開されるオブジェクト モデルがどのように複雑に見えるか、またその理由の詳細については、「[InfoPath 2003 の互換性のあるオブジェクト モデル](../form-templates/infopath-2003-compatible-object-models.md)」のトピックの「COM オブジェクトが InfoPath 2003 互換オブジェクト モデルに公開されるしくみ」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f9380-125">For more information on how and why the object model exposed by an interop assembly appears more complex, see the "How COM Objects are Exposed to Managed Code" section of the [InfoPath 2003 Compatible Object Models](../form-templates/infopath-2003-compatible-object-models.md) topic.</span></span> 
  
### <a name="using-intellisense"></a><span data-ttu-id="f9380-126">IntelliSense を使用する</span><span class="sxs-lookup"><span data-stu-id="f9380-126">Using IntelliSense</span></span>

<span data-ttu-id="f9380-127">このセクションの例では、そのアセンブリへの参照が設定されていることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="f9380-127">The examples in this section assume that you have established references to the Microsoft.Office.Interop.InfoPath and Microsoft.Office.Interop.InfoPath.Xml assemblies.</span></span> <span data-ttu-id="f9380-128">参照およびその他の外部オートメーションの例を設定する方法については、「[外部オートメーションのシナリオと例](external-automation-scenarios-and-examples.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f9380-128">For information on how to set references and additional external automation examples, see [External Automation Scenarios and Examples](external-automation-scenarios-and-examples.md).</span></span>
  
<span data-ttu-id="f9380-129">外部オートメーションコードで Microsoft IntelliSense ステートメントの入力候補を使用するには、次のコード行に示すように、 [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Application.aspx)クラスのインスタンス用のオブジェクト変数を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9380-129">Before you can use Microsoft IntelliSense statement completion in external automation code, you must create an object variable for an instance of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Application.aspx) class as shown in the following line of code.</span></span> 
  
```cs
Application myApp = 
    new Microsoft.Office.Interop.InfoPath.Application();
```

```vb
Dim myApp As Application = _
    New Microsoft.Office.Interop.InfoPath.Application()
```

<span data-ttu-id="f9380-130">オブジェクト変数を作成した後で、変数名に続けてピリオドを入力すると、**Application** クラスの選択できるメンバーのドロップダウン リストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f9380-130">After creating the object variable, when you type the variable name followed by a period, a drop-down list is displayed with members of the **Application** class to select.</span></span> 
  
<span data-ttu-id="f9380-131">InfoPath フォームを操作するには、 [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.XDocument.aspx)型のオブジェクト変数を宣言し、次のコード行に示すように、 **Application**オブジェクト変数の[XDocuments](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.XDocuments.aspx)コレクションからフォームを開いて初期化します。</span><span class="sxs-lookup"><span data-stu-id="f9380-131">To work with an InfoPath form, declare an object variable of type [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.XDocument.aspx) , and then initialize it by opening the form from the [XDocuments](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.XDocuments.aspx) collection of the **Application** object variable as shown in the following line of code.</span></span> 
  
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

<span data-ttu-id="f9380-132">変数の名前とその後のピリオドを入力すると、**XDocument** クラスのメンバーの IntelliSense ステートメント入力候補のドロップダウン リストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f9380-132">The IntelliSense statement completion drop-down list for members of the **XDocument** class will be displayed when you type the name of the variable followed by a period.</span></span> 
  
<span data-ttu-id="f9380-133">Microsoft XML Core Services (MSXML) を使用して、フォームの基になる XML ドキュメントの内容を操作するには、 [IXMLDOMDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Xml.IXMLDOMDocument2.aspx)型の変数を作成し、 **XDocument**クラスの[DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._XDocument2.DOM.aspx)プロパティを使用して、XML を割り当てる必要があります。フォームのドキュメントオブジェクトモデル (DOM) をその変数に格納します。</span><span class="sxs-lookup"><span data-stu-id="f9380-133">To work with the contents of the underlying XML document for the form using Microsoft XML Core Services (MSXML), you must create a variable of type [IXMLDOMDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Xml.IXMLDOMDocument2.aspx) , and then use the [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._XDocument2.DOM.aspx) property of the **XDocument** class to assign the XML Document Object Model (DOM) of the form to that variable.</span></span> 
  
```cs
IXMLDOMDocument2 doc= myXDoc.DOM as IXMLDOMDocument2;
```

```vb
Dim doc As IXMLDOMDocument2 = myXDoc.DOM
```

<span data-ttu-id="f9380-134">変数の名前とその後のピリオドを入力すると、**IXMLDOMDocument2** クラスのメンバーの IntelliSense ステートメント入力候補のドロップダウン リストが表示されるので、MSXML を使用して XML ドキュメントを操作できます。</span><span class="sxs-lookup"><span data-stu-id="f9380-134">The IntelliSense statement completion drop-down list for members of the **IXMLDOMDocument2** class will be displayed when you type the name of the variable followed by a period, which allows you to use MSXML to work with the XML document.</span></span> 
  
### <a name="using-the-class-library-reference-documentation"></a><span data-ttu-id="f9380-135">クラス ライブラリ リファレンス ドキュメントを使用する</span><span class="sxs-lookup"><span data-stu-id="f9380-135">Using the Class Library Reference Documentation</span></span>

<span data-ttu-id="f9380-136">[InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.aspx)名前空間クラスライブラリリファレンスドキュメントの組織は、コクラスインターフェイスと、それらが実装する継承インターフェイスとの関係を反映しています。</span><span class="sxs-lookup"><span data-stu-id="f9380-136">The organization of the [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.aspx) namespace Class Library reference documentation reflects the relationships between coclass interfaces and the inherited interfaces they implement.</span></span> 
  
<span data-ttu-id="f9380-137">[アプリケーション](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Application.aspx)などのコクラスインターフェイスのトピックを開くと、トピックの先頭にあるインターフェイスの説明に続くコクラスインターフェイスのメンバーへのリンクには、空のトピックが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f9380-137">When you open a topic for a coclass interface, such as [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Application.aspx) , the link to the members of the coclass interface following the description of the interface at the beginning of the topic displays an empty topic.</span></span> <span data-ttu-id="f9380-138">コクラス インターフェイスによって実装されるメンバーの一覧を表示するには、そのコクラスによって継承される最も新しいインターフェイスのトピックを開き、そのメンバーの表を開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9380-138">To display the list of members that are implemented by the coclass interface, you must open the topic for the most recent interface that is inherited by the coclass, and then open the table of its members.</span></span> <span data-ttu-id="f9380-139">継承インターフェイスへのリンクは、コクラス インターフェイスのトピックの「解説」セクションの先頭にあります。</span><span class="sxs-lookup"><span data-stu-id="f9380-139">A link to the inherited interface is provided at the beginning of the Remarks section in the coclass interface topic.</span></span> 
  
<span data-ttu-id="f9380-140">Visual Studio コード エディターで F1 キーを押した場合の動作は、大抵の場合インターフェイスのメンバーを操作しているので、F1 ヘルプを呼び出したメンバーが直接表示されることを除いては、ほぼ同様です。</span><span class="sxs-lookup"><span data-stu-id="f9380-140">When you press F1 in the Visual Studio Code Editor, the behavior is similar, except that the member on which you invoke F1 Help will be displayed directly, because you are most typically working with members of an interface.</span></span> <span data-ttu-id="f9380-141">ただし、メンバーがバージョン付きのインターフェイスから実装される場合があるという点で、初めは混乱する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f9380-141">However, the fact that a member can be implemented from a versioned interface may be confusing the first time you encounter it.</span></span> <span data-ttu-id="f9380-142">たとえば、「 `myXDocument.UI.Alert`」と入力し、 `Alert` にカーソルを置いて F1 キーを押すと、「UI2.Alert メソッド」というタイトルのトピックが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f9380-142">For example, if you type  `myXDocument.UI.Alert` and place the cursor on  `Alert` and press F1, a topic titled "UI2.Alert Method" is displayed.</span></span> <span data-ttu-id="f9380-143">これは、 **Alert** メソッドが **UI2** インターフェイスのメンバーの実装であるからです。</span><span class="sxs-lookup"><span data-stu-id="f9380-143">This is because the **Alert** method is an implementation of a member of the **UI2** interface.</span></span> 
  
### <a name="passing-optional-parameters-to-infopath-object-model-members"></a><span data-ttu-id="f9380-144">InfoPath オブジェクト モデルのメンバーにオプションのパラメーターを渡す</span><span class="sxs-lookup"><span data-stu-id="f9380-144">Passing Optional Parameters to InfoPath Object Model Members</span></span>

<span data-ttu-id="f9380-145">InfoPath オブジェクト モデルのメンバーにオプションのパラメーターが含まれており、さらにそのパラメーターの値を指定しない場合は、そのパラメーターの代わりに **Type.Missing** フィールドを渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9380-145">If an InfoPath object model member contains an optional parameter, and you do not specify a value for that parameter, you must pass the **Type.Missing** field for that parameter.</span></span> <span data-ttu-id="f9380-146">実際の値を省略する場合に **Type.Missing** フィールドを渡さないと、ビルド エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f9380-146">Failure to pass the **Type.Missing** field when an actual value is omitted will result in a build error.</span></span> <span data-ttu-id="f9380-147">これは、C# と Visual Basic のどちらで書かれたコードにも当てはまります。</span><span class="sxs-lookup"><span data-stu-id="f9380-147">This is true for code written in both C# and Visual Basic.</span></span> <span data-ttu-id="f9380-148">たとえば、 [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.View2.SelectNodes.aspx) インターフェイスの [SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ViewObject.aspx) メソッドには、  _varEndNode_ と  _varViewContext_ という 2 つのオプション パラメーターが含まれています。</span><span class="sxs-lookup"><span data-stu-id="f9380-148">For example, the [SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.View2.SelectNodes.aspx) method of the [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ViewObject.aspx) interface includes two optional parameters:  _varEndNode_ and  _varViewContext_.</span></span> <span data-ttu-id="f9380-149">これらのオプション パラメーターに対して実際の値を指定しないコード行は、次のようになっている必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9380-149">A line of code that does not specify actual values for these optional parameters should look like the following examples.</span></span>
  
```cs
myXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing);
```

```vb
myXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing)
```

## <a name="see-also"></a><span data-ttu-id="f9380-150">関連項目</span><span class="sxs-lookup"><span data-stu-id="f9380-150">See also</span></span>

- [<span data-ttu-id="f9380-151">外部自動化のシナリオと例</span><span class="sxs-lookup"><span data-stu-id="f9380-151">External automation scenarios and examples</span></span>](external-automation-scenarios-and-examples.md)

