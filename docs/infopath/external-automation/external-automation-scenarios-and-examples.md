---
title: 外部オートメーションのシナリオと例
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2007、[InfoPath 2007] では、プログラムを使用してデータを追加する、オートメーション [InfoPath 2007] フォーム、フォームの外部のシナリオを自動化します。
localization_priority: Normal
ms.assetid: dfa880e6-de23-41c4-b80b-6935e0c8563d
description: Microsoft Office InfoPath プライマリ相互運用機能アセンブリ (Microsoft.Office.Interop.InfoPath.dll) と InfoPath XML 相互運用機能アセンブリ (Microsoft.Office.Interop.InfoPath.Xml.dll) が提供するメンバーは、InfoPath を自動化するためのマネージ コードの記述をサポートします。
ms.openlocfilehash: 1c76e5cb659c9d3f39eec4a7e517ab57c98c858a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799007"
---
# <a name="external-automation-scenarios-and-examples"></a><span data-ttu-id="d7686-104">外部オートメーションのシナリオと例</span><span class="sxs-lookup"><span data-stu-id="d7686-104">External automation scenarios and examples</span></span>

<span data-ttu-id="d7686-105">Microsoft Office InfoPath プライマリ相互運用機能アセンブリ (Microsoft.Office.Interop.InfoPath.dll) と InfoPath XML 相互運用機能アセンブリ (Microsoft.Office.Interop.InfoPath.Xml.dll) が提供するメンバーは、InfoPath を自動化するためのマネージ コードの記述をサポートします。</span><span class="sxs-lookup"><span data-stu-id="d7686-105">The members provided by the Microsoft Office InfoPath primary interop assembly (Microsoft.Office.Interop.InfoPath.dll) and the InfoPath XML interop assembly (Microsoft.Office.Interop.InfoPath.Xml.dll) support writing managed code for automating InfoPath.</span></span> 
  
## <a name="establishing-references-to-the-microsoft-office-infopath-primary-interop-and-infopath-xml-interop-assemblies"></a><span data-ttu-id="d7686-106">Microsoft Office InfoPath プライマリ相互運用機能と InfoPath XML 相互運用機能アセンブリへの参照を確立します。</span><span class="sxs-lookup"><span data-stu-id="d7686-106">Establishing references to the Microsoft Office InfoPath Primary Interop and InfoPath XML Interop assemblies</span></span>

<span data-ttu-id="d7686-107">InfoPath を自動化するためのマネージ コードを記述するには、Microsoft InfoPath のプライマリ相互運用機能と、InfoPath XML 相互運用機能アセンブリへの参照を確立する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d7686-107">To write managed code for automating InfoPath, you must establish references to the Microsoft InfoPath primary interop and the InfoPath XML interop assemblies.</span></span> <span data-ttu-id="d7686-108">Microsoft InfoPath のプライマリ相互運用機能アセンブリは、IPEDITOR によって公開される COM オブジェクト モデルとの相互運用性のサポートを提供します。[Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx)名前空間のメンバーを使用して DLL があります。</span><span class="sxs-lookup"><span data-stu-id="d7686-108">The Microsoft InfoPath primary interop assembly provides support for interoperability with the COM object model exposed by IPEDITOR.DLL by using the members of the [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) namespace.</span></span> <span data-ttu-id="d7686-109">InfoPath XML 相互運用機能アセンブリは、 [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/ja-jp/library/microsoft.office.interop.infopath.xml)名前空間のメンバーを使用して、「Microsoft XML Core Services (MSXML) で公開されている COM オブジェクト モデルとの相互運用性のサポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="d7686-109">The InfoPath XML interop assembly provides support for interoperability with the COM object model exposed by Microsoft XML Core Services (MSXML) by using the members of the [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/ja-jp/library/microsoft.office.interop.infopath.xml) namespace.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="d7686-110">InfoPath を自動化するマネージ コード アプリケーションのユーザーは、InfoPath、Microsoft Office InfoPath のプライマリ相互運用機能アセンブリ、および自分のコンピューターにインストールされている InfoPath XML 相互運用機能アセンブリが必要です。</span><span class="sxs-lookup"><span data-stu-id="d7686-110">Users of managed-code applications that automate InfoPath must have InfoPath, the Microsoft Office InfoPath primary interop assembly, and the InfoPath XML interop assembly installed on their computers.</span></span> <span data-ttu-id="d7686-111">InfoPath セットアップ プログラムで [ **.NET プログラミング サポート**] オプションは、InfoPath の標準的なインストールのため、**マイ コンピューターから実行**に設定されます。</span><span class="sxs-lookup"><span data-stu-id="d7686-111">The **.NET Programmability Support** option in the InfoPath setup program is set to **Run from My Computer** for a typical installation of InfoPath.</span></span>
>  
> <span data-ttu-id="d7686-112">その結果、または.NET Framework 1.1 再配布可能な.NET Framework 1.1 ソフトウェア開発キット (SDK)、またはそれ以降がインストールされている、これらの相互運用機能アセンブリが既定でもインストールされます。</span><span class="sxs-lookup"><span data-stu-id="d7686-112">As a result, as long as the .NET Framework 1.1 Redistributable or .NET Framework 1.1 Software Development Kit (SDK) or later is installed, these interop assemblies will also be installed by default.</span></span> <span data-ttu-id="d7686-113">これらの相互運用機能アセンブリがユーザーのコンピューターで利用できない場合は、する必要があることを確認して、.NET Framework 1.1 以降がインストールされているセットアップを変更し、.NET プログラミングの**を設定する**コントロール パネル**から**プログラムと機能**を実行サポート**InfoPath で **[マイ コンピューターから実行**するためのオプションです。</span><span class="sxs-lookup"><span data-stu-id="d7686-113">If these interop assemblies are not available on a user's computer, you must confirm that the .NET Framework 1.1 or later is installed, and then run **Programs and Features** from the **Control Panel** to change setup and set the **.NET Programmability Support** option of InfoPath to **Run from My Computer**.</span></span> 
  
<span data-ttu-id="d7686-114">次の手順では、Visual Studio プロジェクトに Microsoft Office InfoPath プライマリ相互運用機能アセンブリと InfoPath XML 相互運用機能アセンブリの参照を設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d7686-114">The following procedures describe how to set references to the Microsoft Office InfoPath primary interop and the InfoPath XML interop assemblies in a Visual Studio project.</span></span>
  
<span data-ttu-id="d7686-115">Microsoft.Office.Interop.InfoPath のプライマリ相互運用機能アセンブリへの参照を設定するには、[ **COM** ] タブの [**参照の追加**] ダイアログ ボックスの**Microsoft InfoPath 3.0 のタイプ ライブラリ**への参照を設定します。</span><span class="sxs-lookup"><span data-stu-id="d7686-115">To set a reference to the Microsoft.Office.Interop.InfoPath primary interop assembly, set a reference to **Microsoft InfoPath 3.0 Type Library** on the **COM** tab of the **Add Reference** dialog box.</span></span> <span data-ttu-id="d7686-116">**[COM** ] タブから参照を設定する場合でもグローバル アセンブリ キャッシュ (GAC) に InfoPath セットアップ プログラムによってインストールされる Microsoft.Office.Interop.InfoPath.dll のプライマリ相互運用機能アセンブリへの参照が確立されます。</span><span class="sxs-lookup"><span data-stu-id="d7686-116">Even though you set a reference from the **COM** tab, a reference is established to the Microsoft.Office.Interop.InfoPath.dll primary interop assembly that is installed in the Global Assembly Cache (GAC) by the InfoPath setup program.</span></span> 
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopath-primary-interop-assembly"></a><span data-ttu-id="d7686-117">Microsoft.Office.Interop.InfoPath プライマリ相互運用機能アセンブリへの参照を設定する</span><span class="sxs-lookup"><span data-stu-id="d7686-117">Set a reference to the Microsoft.Office.Interop.InfoPath primary interop assembly</span></span>

1. <span data-ttu-id="d7686-118">Visual Studio のマネージ コード プロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="d7686-118">Open a Visual Studio managed code project.</span></span>
    
2. <span data-ttu-id="d7686-119">**ソリューション エクスプ ローラー**では、**参照**のを右クリックし、 **[参照の追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7686-119">In **Solution Explorer**, right-click **References**, and then click **Add Reference**.</span></span>
    
3. <span data-ttu-id="d7686-120">[ **COM** ] タブでは、 **Microsoft InfoPath 3.0 のタイプ ライブラリ**をダブルクリックし、し、[ **OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7686-120">On the **COM** tab, double-click **Microsoft InfoPath 3.0 Type Library**, and then click **OK**.</span></span>
    
<span data-ttu-id="d7686-121">Microsoft.Office.Interop.InfoPath.Xml の相互運用機能アセンブリへの参照を設定するには、<_ドライブ_> に既定でインストールされている Microsoft.Office.Interop.InfoPath.Xml.dll ファイルを参照: \Program Files\Microsoft Office\OFFICE14 フォルダー.</span><span class="sxs-lookup"><span data-stu-id="d7686-121">To set a reference to the Microsoft.Office.Interop.InfoPath.Xml interop assembly, browse to the Microsoft.Office.Interop.InfoPath.Xml.dll file that is installed by default in the < _drive_>:\Program Files\Microsoft Office\OFFICE14 folder.</span></span> <span data-ttu-id="d7686-122">場合でも、アセンブリのコピーをローカル ファイル システムに指定すると、この手順は、グローバル アセンブリ キャッシュ (GAC) に InfoPath セットアップ プログラムによってインストールされる Microsoft.Office.Interop.InfoPath.Xml.dll のアセンブリへの参照を確立します。</span><span class="sxs-lookup"><span data-stu-id="d7686-122">Even though you specify the copy of the assembly in the local file system, this procedure establishes a reference to the Microsoft.Office.Interop.InfoPath.Xml.dll assembly that is installed in the Global Assembly Cache (GAC) by the InfoPath setup program.</span></span>
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopathxml-interop-assembly"></a><span data-ttu-id="d7686-123">Microsoft.Office.Interop.InfoPath Xml 相互運用機能アセンブリへの参照を設定する</span><span class="sxs-lookup"><span data-stu-id="d7686-123">Set a reference to the Microsoft.Office.Interop.InfoPath.Xml interop assembly</span></span>

1. <span data-ttu-id="d7686-124">開くか、**コンソール アプリケーション**や**Windows アプリケーション**など、Visual Studio のマネージ コード プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="d7686-124">Open or create a Visual Studio managed code project, such as a **Console Application** or **Windows Application**.</span></span>
    
2. <span data-ttu-id="d7686-125">**ソリューション エクスプ ローラー**では、**参照**のを右クリックし、 **[参照の追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7686-125">In **Solution Explorer**, right-click **References**, and then click **Add Reference**.</span></span>
    
3. <span data-ttu-id="d7686-126">[ **.NET** ] タブの [**参照**] をクリックします、<_ドライブ_> に移動: \Program Files\Microsoft Office\OFFICE14 フォルダーでは、[Microsoft.Office.Interop.InfoPath.Xml.dll] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7686-126">On the **.NET** tab, click **Browse**, navigate to the < _drive_>:\Program Files\Microsoft Office\OFFICE14 folder, and then click Microsoft.Office.Interop.InfoPath.Xml.dll.</span></span>
    
4. <span data-ttu-id="d7686-127">[ **OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7686-127">Click **OK**.</span></span>
    
## <a name="automate-changing-the-value-of-a-field"></a><span data-ttu-id="d7686-128">フィールドの値の変更を自動化します。</span><span class="sxs-lookup"><span data-stu-id="d7686-128">Automate changing the value of a field</span></span>

<span data-ttu-id="d7686-129">「企業 A」から「b 社」自分の名前が最近変更された InfoPath の売上報告書フォーム テンプレートのユーザーの顧客の 1 つとします</span><span class="sxs-lookup"><span data-stu-id="d7686-129">Suppose one of the customers of the user of an InfoPath sales report form template recently changed its name from "Company A" to "Company B."</span></span> <span data-ttu-id="d7686-130">開発者が名前の変更を反映するには、このフォーム テンプレートから保存された売上報告書フォームを自動的に更新するコードを記述しようとしています。</span><span class="sxs-lookup"><span data-stu-id="d7686-130">A developer is asked to write code that will automatically update the sales report forms saved from this form template to reflect the name change.</span></span> <span data-ttu-id="d7686-131">次のシナリオでは、様をという名前のフィールドにバインドされているテキスト ボックスを含むフォームを想定しています。</span><span class="sxs-lookup"><span data-stu-id="d7686-131">The following scenario assumes a form that contains a text box that is bound to a field named customerName.</span></span>
  
### <a name="create-the-sample-form-template-and-form"></a><span data-ttu-id="d7686-132">サンプル フォーム テンプレートおよびフォームを作成する</span><span class="sxs-lookup"><span data-stu-id="d7686-132">Create the sample form template and form</span></span>

1. <span data-ttu-id="d7686-133">InfoPath を開き、空白のフォーム テンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="d7686-133">Open InfoPath and create a blank form template.</span></span>
    
2. <span data-ttu-id="d7686-134">フォームに**テキスト ボックス**コントロールを追加し、コントロール様にバインドされているフィールド名を入力します。</span><span class="sxs-lookup"><span data-stu-id="d7686-134">Add a **Text Box** control to the form, and name the field bound to the control customerName.</span></span>
    
3. <span data-ttu-id="d7686-135">[**フィールド**] 作業ウィンドウで、 **[マイフィールド**] フォルダーを右クリックし、[**プロパティ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7686-135">In the **Fields** task pane, right-click the **myFields** folder, and then click **Properties**.</span></span>
    
4. <span data-ttu-id="d7686-136">[**詳細**] タブを選択し、以下の値をコピー **Namespace:**、し、これをメモ帳または取得できる他の場所に貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="d7686-136">On the **Details** tab, select and copy the value following **Namespace:**, and then paste this into Notepad or some other location where you can retrieve it.</span></span> <span data-ttu-id="d7686-137">**SelectionNamespaces**プロパティの値を設定する、コード内のこの値を後で必要があります。</span><span class="sxs-lookup"><span data-stu-id="d7686-137">You will need this value later for setting the value of the **SelectionNamespaces** property in your code.</span></span> 
    
5. <span data-ttu-id="d7686-138">C:\Test という名前のフォルダーにフォーム テンプレートを発行し、既定の名前、Template1 を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="d7686-138">Publish the form template to a folder named C:\Test and accept the default name, Template1.</span></span> 
    
6. <span data-ttu-id="d7686-139">フォーム テンプレートを開いて、「A 社」のテキスト ボックスにフィールドに連結する、得意先名を追加し、"Form1"としてフォームを保存します。</span><span class="sxs-lookup"><span data-stu-id="d7686-139">Open the form template, add the name "Company A" to text box bound to the customerName field, and then save the form as "Form1".</span></span> 
    
### <a name="create-a-managed-code-console-application-to-change-the-name-from-company-a-to-company-b"></a><span data-ttu-id="d7686-140">企業名を「Company A」から「Company B」変更するマネージ コード コンソール アプリケーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="d7686-140">Create a managed code console application to change the name from 'Company A' to 'Company B'</span></span>

1. <span data-ttu-id="d7686-141">Visual Studio を開き、新しい Visual C# または Visual Basic コンソール アプリケーションの UpdateCustomer をという名前を作成します。</span><span class="sxs-lookup"><span data-stu-id="d7686-141">Open Visual Studio and create a new Visual C# or Visual Basic Console Application named UpdateCustomer.</span></span>
    
2. <span data-ttu-id="d7686-142">前述のように、Microsoft Office InfoPath プライマリ相互運用機能アセンブリおよび InfoPath XML 相互運用機能アセンブリのへ参照を確立します。</span><span class="sxs-lookup"><span data-stu-id="d7686-142">Establish references to the Microsoft Office InfoPath primary interop and InfoPath XML interop assemblies as described above.</span></span>
    
3. <span data-ttu-id="d7686-143">Program.cs または Module1.vb ファイル、サンプル フォームを作成したときにコピーした値で、 **SelectionNamespaces**プロパティの設定の名前空間の値を更新することを確認するには、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="d7686-143">Add the following code to the Program.cs or Module1.vb file, making sure to update the value of the namespace in the setting for the **SelectionNamespaces** property with the value you copied when you created the sample form.</span></span> 
    
   ```cs
    using System;
    using System.Collections.Generic;
    using System.Text;
    using Microsoft.Office.Interop.InfoPath;
    using Microsoft.Office.Interop.InfoPath.Xml;
    namespace UpdateCustomer
    {
      class Program
      {
          static void Main(string[] args)
          {
            // Create an InfoPath Application object.
            Application myApp = 
                new Microsoft.Office.Interop.InfoPath.Application();
            // Get a reference the XDocuments collection 
            // and open the sample form.
            XDocumentsCollection myXDocs = myApp.XDocuments;
            XDocument myXDoc = myXDocs.Open("C:\\Test\\Form1.xml",
                (int) XdDocumentVersionMode.xdFailOnVersionOlder);
            
            // Access the XML DOM for the underlying XML document using
            // the DOM property. Note that you must cast to the 
            // IXMLDOMDocument2 type from the
            // Microsoft.Office.Interop.InfoPath.Xml namespace
            // to access the XML DOM.
            IXMLDOMDocument2 myXMLDoc = myXDoc.DOM as IXMLDOMDocument2;
            // Set the MSXML SelectionNamespaces property to the my
            // namespace of the form. IMPORTANT:Replace the namespace 
            // value below with that of your sample form.
            myXMLDoc.setProperty("SelectionNamespaces",
    "xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2006-09-06T23:17:34'");
            // Select all instances of customerName that contain 
            //'Company A'.
            IXMLDOMNodeList myNames = 
                myXMLDoc.selectNodes(
                "//my:customerName[. = 'Company A']");
            // Check to determine if any nodes were returned.
            if (myNames.length < 1)
            Console.WriteLine(
                "No elements containing 'Company A' were found.");
            // Loop through the list updating to 'Company B'.
            IXMLDOMNode myName = myNames.nextNode();
            while (myName != null)
            {
                myName.text = "Company B";
                myName = myNames.nextNode();
            }
            // Save the updated form as Form2.xml and close out.
            myXDoc.SaveAs("C:\\Test\\Form2.xml");
            myXDocs.Close(0);
            myApp.Quit(false);
            Console.WriteLine("Finished!");
          }
      }
    }
   ```

   ```vb
    Imports Microsoft.Office.Interop.InfoPath
    Imports Microsoft.Office.Interop.InfoPath.Xml
    Module Module1
      Sub Main()
          ' Create an InfoPath Application object.
          Dim myApp As Application = _
            New Microsoft.Office.Interop.InfoPath.Application()
          ' Get a reference the XDocuments collection 
          ' and open the sample form.
          Dim myXDocs As XDocumentsCollection = myApp.XDocuments
          Dim myXDoc As XDocument = myXDocs.Open( _
            "C:\\Test\\Form1.xml", _
            XdDocumentVersionMode.xdFailOnVersionOlder)
          ' Access the XML DOM for the underlying XML document using
          ' the DOM property. Note that you must cast to the 
          ' IXMLDOMDocument2 type from the
          ' Microsoft.Office.Interop.InfoPath.Xml namespace
          ' to access the XML DOM.
          Dim myXMLDoc As IXMLDOMDocument2 = _
            DirectCast(myXDoc.DOM, IXMLDOMDocument2)
          ' Set the MSXML SelectionNamespaces property to the my
          ' namespace of the form. IMPORTANT:Replace the namespace 
          ' value below with that of your sample form.
          myXMLDoc.setProperty("SelectionNamespaces", _
    "xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2006-09-06T23:17:34'")
          ' Select all instances of customerName that contain 
          ''Company A'.
          Dim myNames As IXMLDOMNodeList = _
      myXMLDoc.selectNodes("//my:customerName[. = 'Company A']")
          ' Check to determine if any nodes were returned.
          If (myNames.length < 1) Then
            Console.WriteLine( _
                "No elements containing 'Company A' were found.")
          Else
            ' Loop through the list updating to 'Company B'.
            Dim myName As IXMLDOMNode = myNames.nextNode()
            While (myName IsNot Nothing)
                myName.text = "Company B"
                myName = myNames.nextNode()
            End While
          End If
          ' Save the updated form as Form2.xml and close out.
          myXDoc.SaveAs("C:\\Test\\Form2.xml")
          myXDocs.Close(0)
          myApp.Quit(False)
          Console.WriteLine("Finished!")
      End Sub
    End Module
    
   ```

4. <span data-ttu-id="d7686-144">コンパイルしてコンソール アプリケーションを実行するのには [**デバッグ**] メニューの [**デバッグ開始**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7686-144">Click **Start Debugging** on the **Debug** menu to compile and run the console application.</span></span> 
    
   <span data-ttu-id="d7686-145">アプリケーションは、Form1.xml、会社 A の値が含まれている得意先のすべての要素をループとして保存したフォームを開き、会社 B にその値を変更操作が完了すると、C:\Test フォルダー内の Form2.xml として、フォームの新しいコピーが保存されます。</span><span class="sxs-lookup"><span data-stu-id="d7686-145">The application opens the form saved as Form1.xml and loops through all customerName elements that contain the value Company A and changes that value to Company B. When the operation is complete, a new copy of the form is saved as Form2.xml in the C:\Test folder.</span></span> 
    
## <a name="automate-opening-a-form-and-populating-field-values"></a><span data-ttu-id="d7686-146">フォームを開くと、フィールドの値を設定を自動化します。</span><span class="sxs-lookup"><span data-stu-id="d7686-146">Automate opening a form and populating field values</span></span>

<span data-ttu-id="d7686-147">次の使用例は、空白のフォームを開き、名、姓、名、およびフォームのフィールドのアドレスを作成を自動化します。</span><span class="sxs-lookup"><span data-stu-id="d7686-147">The following example automates opening a blank form and populating the first name, last name, and address fields in the form.</span></span> <span data-ttu-id="d7686-148">このシナリオでは、という名前の姓、姓、およびアドレスのフィールドにバインドされている 3 つのテキスト ボックスを含むフォームを想定しています。</span><span class="sxs-lookup"><span data-stu-id="d7686-148">This scenario assumes a form that contains three text boxes that are bound to fields named FirstName, LastName, and Address.</span></span>
  
### <a name="create-the-sample-form-template-and-form"></a><span data-ttu-id="d7686-149">サンプル フォーム テンプレートおよびフォームを作成する</span><span class="sxs-lookup"><span data-stu-id="d7686-149">Create the sample form template and form</span></span>

1. <span data-ttu-id="d7686-150">InfoPath を開き、空白のフォームを作成します。</span><span class="sxs-lookup"><span data-stu-id="d7686-150">Open InfoPath and create a blank form.</span></span>
    
2. <span data-ttu-id="d7686-151">3 つのテキスト ボックス コントロールをフォームに追加し、コントロールにバインドされたフィールドの名前: 姓、姓、およびアドレス。</span><span class="sxs-lookup"><span data-stu-id="d7686-151">Add three text box controls to the form, and name the fields bound to the controls: FirstName, LastName, and Address.</span></span> <span data-ttu-id="d7686-152">必要なその他のフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="d7686-152">Add any other fields you want.</span></span>
    
3. <span data-ttu-id="d7686-153">[**フィールド**] 作業ウィンドウで、 **[マイフィールド**] フォルダーを右クリックし、[**プロパティ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7686-153">In the **Fields** task pane, right-click the **myFields** folder, and then click **Properties**.</span></span>
    
4. <span data-ttu-id="d7686-154">[**詳細**] タブを選択し、以下の値をコピー **Namespace:**、し、これをメモ帳または取得できる他の場所に貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="d7686-154">On the **Details** tab, select and copy the value following **Namespace:**, and then paste this into Notepad or some other location where you can retrieve it.</span></span> <span data-ttu-id="d7686-155">**SelectionNamespaces**プロパティの値を設定する、コード内のこの値を後で必要があります。</span><span class="sxs-lookup"><span data-stu-id="d7686-155">You will need this value later for setting the value of the **SelectionNamespaces** property in your code.</span></span> 
    
5. <span data-ttu-id="d7686-156">C:\Test という名前のフォルダーにフォーム テンプレートを発行し、「Template1」という既定の名前とします。</span><span class="sxs-lookup"><span data-stu-id="d7686-156">Publish the form template to a folder named C:\Temp and accept the default name, Template1.</span></span>
    
6. <span data-ttu-id="d7686-157">フォーム テンプレートを開き、空白のフォームを C:\Temp に「Form1」として保存します。</span><span class="sxs-lookup"><span data-stu-id="d7686-157">Open the form template and save a blank form as "Form1" to C:\Temp.</span></span>
    
### <a name="create-a-managed-code-console-application-to-open-the-form-and-populate-the-fields"></a><span data-ttu-id="d7686-158">マネージ コード コンソール アプリケーションを作成し、フォームを開いてフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="d7686-158">Create a managed code console application to open the form and populate the fields</span></span>

1. <span data-ttu-id="d7686-159">Visual Studio を開き、「OpenForm」という名前で新しい Visual C# または Visual Basic コンソール アプリケーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="d7686-159">Open Visual Studio and create a new Visual C# or Visual Basic Console Application named OpenForm.</span></span>
    
2. <span data-ttu-id="d7686-160">前述のように、Microsoft Office InfoPath プライマリ相互運用機能アセンブリおよび InfoPath XML 相互運用機能アセンブリのへ参照を確立します。</span><span class="sxs-lookup"><span data-stu-id="d7686-160">Establish references to the Microsoft Office InfoPath primary interop and InfoPath XML interop assemblies as described above.</span></span>
    
3. <span data-ttu-id="d7686-161">Program.cs または Module1.vb ファイル、サンプル フォームを作成したときにコピーした値で、 **SelectionNamespaces**プロパティの設定の名前空間の値を更新することを確認するには、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="d7686-161">Add the following code to the Program.cs or Module1.vb file, making sure to update the value of the namespace in the setting for the **SelectionNamespaces** property with the value you copied when you created the sample form.</span></span> 
    
   ```cs
    using System;
    using System.Collections.Generic;
    using System.Text;
    using Microsoft.Office.Interop.InfoPath;
    using Microsoft.Office.Interop.InfoPath.Xml;
    namespace OpenForm
    {
      class Program
      {
          static void Main(string[] args)
          {
            // Create an InfoPath Application object.
            Application myApp=
                new Microsoft.Office.Interop.InfoPath.Application();
            // Create an InfoPath XDocument variable and open 
            // the blank form.
            XDocument myXDoc = myApp.XDocuments.Open(
                "c:\\temp\\Form1.xml",
                (int) XdDocumentVersionMode.xdFailOnVersionOlder);
            
            // Create an IXMLDOMDocument2 variable and access 
            // the XML DOM from the underlying XML document
            // using the DOM property of the XDocument object. 
            // Note that you must cast to IXMLDOMDocument2 to do so.
            IXMLDOMDocument2 doc= myXDoc.DOM as IXMLDOMDocument2;
            // Set the MSXML SelectionNamespaces property to the my
            // namespace of the form. IMPORTANT:Replace the namespace
            // value below with that of your sample form.
            doc.setProperty("SelectionNamespaces","xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2006-09-06T23:17:34'");
            // Pre-populate the fields with specified values.
            doc.selectSingleNode("//my:FirstName").text="My Name";
            doc.selectSingleNode("//my:LastName").text="My LastName";
            doc.selectSingleNode("//my:Address").text="My Address";
            // Save the form, leaving InfoPath open.
            myXDoc.Save();
            
          }
      }
    }
   ```

   ```vb
    Imports Microsoft.Office.Interop.InfoPath
    Imports Microsoft.Office.Interop.InfoPath.Xml
    Module Module1
      Sub Main()
          ' Create an InfoPath Application object.
          Dim myApp As Application = _
            New Microsoft.Office.Interop.InfoPath.Application
          ' Create an InfoPath XDocument variable and open 
          ' the blank form.
          Dim myXDoc As XDocument = myApp.XDocuments.Open( _
            "c:\\temp\\Form1.xml", _
            XdDocumentVersionMode.xdFailOnVersionOlder)
          ' Create an IXMLDOMDocument2 variable and access 
          ' the XML DOM from the underlying XML document
          ' using the DOM property of the XDocument object.
          Dim doc As IXMLDOMDocument2 = myXDoc.DOM
          ' Set the MSXML SelectionNamespaces property to the my
          ' namespace of the form. IMPORTANT:Replace the namespace
          ' value below with that of your sample form.
          doc.setProperty("SelectionNamespaces", "xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2006-09-06T23:17:34'")
          ' Pre-populate the fields with specified values.
          doc.selectSingleNode("//my:FirstName").text = "My Name"
          doc.selectSingleNode("//my:LastName").text = "My LastName"
          doc.selectSingleNode("//my:Address").text = "My Address"
          ' Save the form, leaving InfoPath open.
          myXDoc.Save()
      End Sub
    End Module
    
   ```

4. <span data-ttu-id="d7686-162">**[デバッグ**] メニューの [**デバッグの開始**をコンパイルしてコンソール アプリケーションを実行するをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7686-162">On the **Debug** menu, click **Start Debugging** to compile and run the console application.</span></span> 
    
   <span data-ttu-id="d7686-163">アプリケーションは Form1.xml として保存するフォームを開くコードでは、指定した値で、[部署名]、[姓]、およびアドレス フィールドに入力および InfoPath を開いたまま、フォームを保存します。</span><span class="sxs-lookup"><span data-stu-id="d7686-163">The application will open the form saved as Form1.xml and fill in the FirstName, LastName, and Address fields with the values specified in the code, and then save the form, leaving InfoPath open.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="d7686-164">関連項目</span><span class="sxs-lookup"><span data-stu-id="d7686-164">See also</span></span>

- [<span data-ttu-id="d7686-165">Microsoft Office InfoPath のプライマリ相互運用機能アセンブリについて</span><span class="sxs-lookup"><span data-stu-id="d7686-165">About the Microsoft Office InfoPath Primary Interop Assembly</span></span>](about-the-microsoft-office-infopath-primary-interop-assembly.md)
- [<span data-ttu-id="d7686-166">InfoPath XML 相互運用機能アセンブリについて</span><span class="sxs-lookup"><span data-stu-id="d7686-166">About the InfoPath XML Interop Assembly</span></span>](about-the-infopath-xml-interop-assembly.md)

