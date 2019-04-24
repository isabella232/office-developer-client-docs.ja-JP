---
title: 外部自動化のシナリオと例
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2007、フォーム [infopath 2007] の自動化、プログラムによるデータの追加、オートメーション [infopath 2007]、外部シナリオ
localization_priority: Normal
ms.assetid: dfa880e6-de23-41c4-b80b-6935e0c8563d
description: Microsoft Office InfoPath プライマリ相互運用機能アセンブリ (Microsoft.Office.Interop.InfoPath.dll) と InfoPath XML 相互運用機能アセンブリ (Microsoft.Office.Interop.InfoPath.Xml.dll) が提供するメンバーは、InfoPath を自動化するためのマネージ コードの記述をサポートします。
ms.openlocfilehash: af8bfbb0322b9d70fb85ba21a757a581ba423a44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310200"
---
# <a name="external-automation-scenarios-and-examples"></a><span data-ttu-id="d0c89-104">外部自動化のシナリオと例</span><span class="sxs-lookup"><span data-stu-id="d0c89-104">External automation scenarios and examples</span></span>

<span data-ttu-id="d0c89-105">Microsoft Office InfoPath プライマリ相互運用機能アセンブリ (Microsoft.Office.Interop.InfoPath.dll) と InfoPath XML 相互運用機能アセンブリ (Microsoft.Office.Interop.InfoPath.Xml.dll) が提供するメンバーは、InfoPath を自動化するためのマネージ コードの記述をサポートします。</span><span class="sxs-lookup"><span data-stu-id="d0c89-105">The members provided by the Microsoft Office InfoPath primary interop assembly (Microsoft.Office.Interop.InfoPath.dll) and the InfoPath XML interop assembly (Microsoft.Office.Interop.InfoPath.Xml.dll) support writing managed code for automating InfoPath.</span></span> 
  
## <a name="establishing-references-to-the-microsoft-office-infopath-primary-interop-and-infopath-xml-interop-assemblies"></a><span data-ttu-id="d0c89-106">Microsoft Office InfoPath プライマリ相互運用機能アセンブリと infopath XML 相互運用機能アセンブリへの参照を確立する</span><span class="sxs-lookup"><span data-stu-id="d0c89-106">Establishing references to the Microsoft Office InfoPath Primary Interop and InfoPath XML Interop assemblies</span></span>

<span data-ttu-id="d0c89-107">InfoPath を自動化するためのマネージ コードを記述するには、Microsoft InfoPath プライマリ相互運用機能アセンブリと、InfoPath XML 相互運用機能アセンブリの参照を確立する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d0c89-107">To write managed code for automating InfoPath, you must establish references to the Microsoft InfoPath primary interop and the InfoPath XML interop assemblies.</span></span> <span data-ttu-id="d0c89-108">Microsoft InfoPath プライマリ相互運用機能アセンブリは、ipeditor が公開する COM オブジェクトモデルとの相互運用性のサポートを提供します。DLL の場合は、この名前[](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx)空間のメンバーを使用します。</span><span class="sxs-lookup"><span data-stu-id="d0c89-108">The Microsoft InfoPath primary interop assembly provides support for interoperability with the COM object model exposed by IPEDITOR.DLL by using the members of the [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) namespace.</span></span> <span data-ttu-id="d0c89-109">infopath xml 相互運用機能アセンブリは、microsoft xml Core Services (MSXML) によって公開されている COM オブジェクトモデルとの相互[](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml)運用性をサポートします。</span><span class="sxs-lookup"><span data-stu-id="d0c89-109">The InfoPath XML interop assembly provides support for interoperability with the COM object model exposed by Microsoft XML Core Services (MSXML) by using the members of the [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml) namespace.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="d0c89-110">InfoPath を自動化するマネージ コード アプリケーションのユーザーは、InfoPath と、Microsoft Office InfoPath プライマリ相互運用機能アセンブリと、ユーザーのコンピューターにインストールされている InfoPath XML 相互運用機能アセンブリが必要です。</span><span class="sxs-lookup"><span data-stu-id="d0c89-110">Users of managed-code applications that automate InfoPath must have InfoPath, the Microsoft Office InfoPath primary interop assembly, and the InfoPath XML interop assembly installed on their computers.</span></span> <span data-ttu-id="d0c89-111">infopath セットアッププログラムの **.net プログラミングサポート**オプションは、infopath の標準的なインストールのために**マイコンピューターから実行**するように設定されています。</span><span class="sxs-lookup"><span data-stu-id="d0c89-111">The **.NET Programmability Support** option in the InfoPath setup program is set to **Run from My Computer** for a typical installation of InfoPath.</span></span>
>  
> <span data-ttu-id="d0c89-112">その結果、.NET Framework 1.1 再配布可能バージョン、あるいは.NET Framework 1.1 以降のソフトウェア開発キット (SDK) がインストールされていれば、相互運用機能アセンブリも既定でインストールされます。</span><span class="sxs-lookup"><span data-stu-id="d0c89-112">As a result, as long as the .NET Framework 1.1 Redistributable or .NET Framework 1.1 Software Development Kit (SDK) or later is installed, these interop assemblies will also be installed by default.</span></span> <span data-ttu-id="d0c89-113">これらの相互運用機能アセンブリがユーザーのコンピューターで使用できない場合は、.net Framework 1.1 以降がインストールされていることを確認してから、[**コントロールパネル]** から [**プログラムと機能**] を実行して、セットアップを変更し、 **.net プログラミングを設定します。** InfoPath のサポートオプションが**マイコンピューターから実行**されます。</span><span class="sxs-lookup"><span data-stu-id="d0c89-113">If these interop assemblies are not available on a user's computer, you must confirm that the .NET Framework 1.1 or later is installed, and then run **Programs and Features** from the **Control Panel** to change setup and set the **.NET Programmability Support** option of InfoPath to **Run from My Computer**.</span></span> 
  
<span data-ttu-id="d0c89-114">次の手順では、Visual Studio プロジェクトに Microsoft Office InfoPath プライマリ相互運用機能アセンブリと InfoPath XML 相互運用機能アセンブリの参照を設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d0c89-114">The following procedures describe how to set references to the Microsoft Office InfoPath primary interop and the InfoPath XML interop assemblies in a Visual Studio project.</span></span>
  
<span data-ttu-id="d0c89-p104">Microsoft.Office.Interop.InfoPath プライマリ相互運用機能アセンブリの参照を設定するには、**[参照の追加]** ダイアログ ボックスの **[COM]** タブ上で **Microsoft InfoPath 3.0 タイプ ライブラリ**の参照を設定します。**[COM]** タブから参照を設定するものの、InfoPath セットアップ プログラムがグローバル アセンブリ キャッシュ (GAC) にインストールした Microsoft.Office.Interop.InfoPath.dll プライマリ相互運用機能アセンブリへの参照が確立されます。</span><span class="sxs-lookup"><span data-stu-id="d0c89-p104">To set a reference to the Microsoft.Office.Interop.InfoPath primary interop assembly, set a reference to **Microsoft InfoPath 3.0 Type Library** on the **COM** tab of the **Add Reference** dialog box. Even though you set a reference from the **COM** tab, a reference is established to the Microsoft.Office.Interop.InfoPath.dll primary interop assembly that is installed in the Global Assembly Cache (GAC) by the InfoPath setup program.</span></span> 
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopath-primary-interop-assembly"></a><span data-ttu-id="d0c89-117">Microsoft.Office.Interop.InfoPath プライマリ相互運用機能アセンブリへの参照を設定する</span><span class="sxs-lookup"><span data-stu-id="d0c89-117">Set a reference to the Microsoft.Office.Interop.InfoPath primary interop assembly</span></span>

1. <span data-ttu-id="d0c89-118">Visual Studio のマネージ コード プロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="d0c89-118">Open a Visual Studio managed code project.</span></span>
    
2. <span data-ttu-id="d0c89-119">**ソリューション エクスプローラー**で [**参照**] を右クリックし、[**参照の追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d0c89-119">In **Solution Explorer**, right-click **References**, and then click **Add Reference**.</span></span>
    
3. <span data-ttu-id="d0c89-120">**[COM]** タブの **[Microsoft InfoPath 3.0 タイプ ライブラリ]** をダブルクリックし、**[OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d0c89-120">On the **COM** tab, double-click **Microsoft InfoPath 3.0 Type Library**, and then click **OK**.</span></span>
    
<span data-ttu-id="d0c89-121">< の相互運用機能アセンブリへの参照を設定するには、既定でインストールされているファイルを参照します。このファイルは、既定では、>:/会社__ の Office\OFFICE14 フォルダーにあります。.</span><span class="sxs-lookup"><span data-stu-id="d0c89-121">To set a reference to the Microsoft.Office.Interop.InfoPath.Xml interop assembly, browse to the Microsoft.Office.Interop.InfoPath.Xml.dll file that is installed by default in the < _drive_>:\Program Files\Microsoft Office\OFFICE14 folder.</span></span> <span data-ttu-id="d0c89-122">ローカル ファイル システムのアセンブリのコピーを指定しても、この手順では InfoPath セットアップ プログラムがグローバル アセンブリ キャッシュ (GAC) にインストールした Microsoft.Office.Interop.InfoPath.Xml.dll アセンブリへの参照が確立されます。</span><span class="sxs-lookup"><span data-stu-id="d0c89-122">Even though you specify the copy of the assembly in the local file system, this procedure establishes a reference to the Microsoft.Office.Interop.InfoPath.Xml.dll assembly that is installed in the Global Assembly Cache (GAC) by the InfoPath setup program.</span></span>
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopathxml-interop-assembly"></a><span data-ttu-id="d0c89-123">Microsoft.Office.Interop.InfoPath Xml 相互運用機能アセンブリへの参照を設定する</span><span class="sxs-lookup"><span data-stu-id="d0c89-123">Set a reference to the Microsoft.Office.Interop.InfoPath.Xml interop assembly</span></span>

1. <span data-ttu-id="d0c89-124">**コンソール アプリケーション**または **Windows アプリケーション**などの Visual Studio マネージ コード プロジェクトを開くか、作成します。</span><span class="sxs-lookup"><span data-stu-id="d0c89-124">Open or create a Visual Studio managed code project, such as a **Console Application** or **Windows Application**.</span></span>
    
2. <span data-ttu-id="d0c89-125">**ソリューション エクスプローラー**で [**参照**] を右クリックし、[**参照の追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d0c89-125">In **Solution Explorer**, right-click **References**, and then click **Add Reference**.</span></span>
    
3. <span data-ttu-id="d0c89-126">[ **.net** ] タブで、[**参照**] をクリックして、< _drive_>: Office\OFFICE14 フォルダーに移動し、次に [Microsoft] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d0c89-126">On the **.NET** tab, click **Browse**, navigate to the < _drive_>:\Program Files\Microsoft Office\OFFICE14 folder, and then click Microsoft.Office.Interop.InfoPath.Xml.dll.</span></span>
    
4. <span data-ttu-id="d0c89-127">**[OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d0c89-127">Click **OK**.</span></span>
    
## <a name="automate-changing-the-value-of-a-field"></a><span data-ttu-id="d0c89-128">フィールドの値の変更を自動化する</span><span class="sxs-lookup"><span data-stu-id="d0c89-128">Automate changing the value of a field</span></span>

<span data-ttu-id="d0c89-129">InfoPath の売上報告書フォーム テンプレートのユーザーの顧客企業の 1 社が「Company A」から「Company B」に自社名を先日変更したとします。</span><span class="sxs-lookup"><span data-stu-id="d0c89-129">Suppose one of the customers of the user of an InfoPath sales report form template recently changed its name from "Company A" to "Company B."</span></span> <span data-ttu-id="d0c89-130">開発者は、このフォーム テンプレートから保存された売上報告書フォームを自動的に更新して社名変更を反映するコードを記述するように依頼されました。</span><span class="sxs-lookup"><span data-stu-id="d0c89-130">A developer is asked to write code that will automatically update the sales report forms saved from this form template to reflect the name change.</span></span> <span data-ttu-id="d0c89-131">次のシナリオでは、[customerName] フィールドにバインドされたテキスト ボックスを含むフォームを想定します。</span><span class="sxs-lookup"><span data-stu-id="d0c89-131">The following scenario assumes a form that contains a text box that is bound to a field named customerName.</span></span>
  
### <a name="create-the-sample-form-template-and-form"></a><span data-ttu-id="d0c89-132">サンプル フォーム テンプレートおよびフォームを作成する</span><span class="sxs-lookup"><span data-stu-id="d0c89-132">Create the sample form template and form</span></span>

1. <span data-ttu-id="d0c89-133">InfoPath を開き、空白のフォーム テンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="d0c89-133">Open InfoPath and create a blank form template.</span></span>
    
2. <span data-ttu-id="d0c89-134">フォームに**テキストボックス**コントロールを追加し、コントロールにバインドされたフィールドの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="d0c89-134">Add a **Text Box** control to the form, and name the field bound to the control customerName.</span></span>
    
3. <span data-ttu-id="d0c89-135">**[フィールド]** タスク ウィンドウの **[マイフィールド]** フォルダーを右クリックし、**[プロパティ]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d0c89-135">In the **Fields** task pane, right-click the **myFields** folder, and then click **Properties**.</span></span>
    
4. <span data-ttu-id="d0c89-136">**[詳細]** タブから、次の値の **[名前空間:]** に続く値を選択してコピーし、これをメモ帳または取得できる他の場所に貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="d0c89-136">On the **Details** tab, select and copy the value following **Namespace:**, and then paste this into Notepad or some other location where you can retrieve it.</span></span> <span data-ttu-id="d0c89-137">この値は、コード内の **SelectionNamespaces** プロパティの値を設定する時に必要になります。</span><span class="sxs-lookup"><span data-stu-id="d0c89-137">You will need this value later for setting the value of the **SelectionNamespaces** property in your code.</span></span> 
    
5. <span data-ttu-id="d0c89-138">C:\Test という名前のフォルダーにフォーム テンプレートを発行し、「Template1」という既定の名前とします。</span><span class="sxs-lookup"><span data-stu-id="d0c89-138">Publish the form template to a folder named C:\Test and accept the default name, Template1.</span></span> 
    
6. <span data-ttu-id="d0c89-139">フォーム テンプレートを開き、[customerName] フィールドにバインドされているテキストボックスに「Company A」を入力し、フォームを「Form1」として保存します。</span><span class="sxs-lookup"><span data-stu-id="d0c89-139">Open the form template, add the name "Company A" to text box bound to the customerName field, and then save the form as "Form1".</span></span> 
    
### <a name="create-a-managed-code-console-application-to-change-the-name-from-company-a-to-company-b"></a><span data-ttu-id="d0c89-140">企業名を「Company A」から「Company B」変更するマネージ コード コンソール アプリケーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="d0c89-140">Create a managed code console application to change the name from 'Company A' to 'Company B'</span></span>

1. <span data-ttu-id="d0c89-141">Visual Studio を開き、[UpdateCustomer]という名前で新しい Visual C# または Visual Basic コンソール アプリケーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="d0c89-141">Open Visual Studio and create a new Visual C# or Visual Basic Console Application named UpdateCustomer.</span></span>
    
2. <span data-ttu-id="d0c89-142">前述のように、Microsoft Office InfoPath プライマリ相互運用機能アセンブリおよび InfoPath XML 相互運用機能アセンブリのへ参照を確立します。</span><span class="sxs-lookup"><span data-stu-id="d0c89-142">Establish references to the Microsoft Office InfoPath primary interop and InfoPath XML interop assemblies as described above.</span></span>
    
3. <span data-ttu-id="d0c89-143">次のコードを Program.cs または Module1.vb ファイルに追加し、サンプル フォームを作成したときにコピーした値に、**SelectionNamespaces** プロパティ設定の名前空間の値が更新されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d0c89-143">Add the following code to the Program.cs or Module1.vb file, making sure to update the value of the namespace in the setting for the **SelectionNamespaces** property with the value you copied when you created the sample form.</span></span> 
    
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
    "xmlns:my='https://schemas.microsoft.com/office/infopath/2003/myXSD/2006-09-06T23:17:34'");
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
    "xmlns:my='https://schemas.microsoft.com/office/infopath/2003/myXSD/2006-09-06T23:17:34'")
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

4. <span data-ttu-id="d0c89-144">**[デバッグ]** メニューの **[デバッグの開始]** をクリックし、コンソール アプリケーションをコンパイルして実行します。</span><span class="sxs-lookup"><span data-stu-id="d0c89-144">Click **Start Debugging** on the **Debug** menu to compile and run the console application.</span></span> 
    
   <span data-ttu-id="d0c89-145">アプリケーションは Form1.xml として保存されているフォームを開き、「Company A」という値を含むすべての customerName 要素をループし、その値を「Company B」に変更します。操作が完了すると、フォームの新しいコピーが C:\Test フォルダーに Form2.xml として保存されます。</span><span class="sxs-lookup"><span data-stu-id="d0c89-145">The application opens the form saved as Form1.xml and loops through all customerName elements that contain the value Company A and changes that value to Company B. When the operation is complete, a new copy of the form is saved as Form2.xml in the C:\Test folder.</span></span> 
    
## <a name="automate-opening-a-form-and-populating-field-values"></a><span data-ttu-id="d0c89-146">フォームを開いてフィールド値を入力する処理を自動化する</span><span class="sxs-lookup"><span data-stu-id="d0c89-146">Automate opening a form and populating field values</span></span>

<span data-ttu-id="d0c89-147">次の例では、空白のフォームを開き、フォームの名、姓、アドレスの各フィールドを設定する操作を自動で行います。</span><span class="sxs-lookup"><span data-stu-id="d0c89-147">The following example automates opening a blank form and populating the first name, last name, and address fields in the form.</span></span> <span data-ttu-id="d0c89-148">このシナリオでは、“名”、“姓”、“アドレス” という名前の各フィールドにバインドされた 3 つのテキスト ボックスを含むフォームを想定します。</span><span class="sxs-lookup"><span data-stu-id="d0c89-148">This scenario assumes a form that contains three text boxes that are bound to fields named FirstName, LastName, and Address.</span></span>
  
### <a name="create-the-sample-form-template-and-form"></a><span data-ttu-id="d0c89-149">サンプル フォーム テンプレートおよびフォームを作成する</span><span class="sxs-lookup"><span data-stu-id="d0c89-149">Create the sample form template and form</span></span>

1. <span data-ttu-id="d0c89-150">InfoPath を開き、空白のフォームを作成します。</span><span class="sxs-lookup"><span data-stu-id="d0c89-150">Open InfoPath and create a blank form.</span></span>
    
2. <span data-ttu-id="d0c89-151">テキスト ボックス コントロールを 3 つ追加し、コントロールにバインドされたフィールドの名前を“名”、“姓”、“アドレス” にします。</span><span class="sxs-lookup"><span data-stu-id="d0c89-151">Add three text box controls to the form, and name the fields bound to the controls: FirstName, LastName, and Address.</span></span> <span data-ttu-id="d0c89-152">必要なその他のフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="d0c89-152">Add any other fields you want.</span></span>
    
3. <span data-ttu-id="d0c89-153">**[フィールド]** タスク ウィンドウの **[マイフィールド]** フォルダーを右クリックし、**[プロパティ]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d0c89-153">In the **Fields** task pane, right-click the **myFields** folder, and then click **Properties**.</span></span>
    
4. <span data-ttu-id="d0c89-154">**[詳細]** タブから、次の値の **[名前空間:]** に続く値を選択してコピーし、これをメモ帳または取得できる他の場所に貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="d0c89-154">On the **Details** tab, select and copy the value following **Namespace:**, and then paste this into Notepad or some other location where you can retrieve it.</span></span> <span data-ttu-id="d0c89-155">この値は、コード内の **SelectionNamespaces** プロパティの値を設定する時に必要になります。</span><span class="sxs-lookup"><span data-stu-id="d0c89-155">You will need this value later for setting the value of the **SelectionNamespaces** property in your code.</span></span> 
    
5. <span data-ttu-id="d0c89-156">C:\Test という名前のフォルダーにフォーム テンプレートを発行し、「Template1」という既定の名前とします。</span><span class="sxs-lookup"><span data-stu-id="d0c89-156">Publish the form template to a folder named C:\Temp and accept the default name, Template1.</span></span>
    
6. <span data-ttu-id="d0c89-157">フォーム テンプレートを開き、空白のフォームを C:\Temp に「Form1」として保存します。</span><span class="sxs-lookup"><span data-stu-id="d0c89-157">Open the form template and save a blank form as "Form1" to C:\Temp.</span></span>
    
### <a name="create-a-managed-code-console-application-to-open-the-form-and-populate-the-fields"></a><span data-ttu-id="d0c89-158">マネージ コード コンソール アプリケーションを作成し、フォームを開いてフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="d0c89-158">Create a managed code console application to open the form and populate the fields</span></span>

1. <span data-ttu-id="d0c89-159">Visual Studio を開き、「OpenForm」という名前で新しい Visual C# または Visual Basic コンソール アプリケーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="d0c89-159">Open Visual Studio and create a new Visual C# or Visual Basic Console Application named OpenForm.</span></span>
    
2. <span data-ttu-id="d0c89-160">前述のように、Microsoft Office InfoPath プライマリ相互運用機能アセンブリおよび InfoPath XML 相互運用機能アセンブリのへ参照を確立します。</span><span class="sxs-lookup"><span data-stu-id="d0c89-160">Establish references to the Microsoft Office InfoPath primary interop and InfoPath XML interop assemblies as described above.</span></span>
    
3. <span data-ttu-id="d0c89-161">次のコードを Program.cs または Module1.vb ファイルに追加し、サンプル フォームを作成したときにコピーした値に、**SelectionNamespaces** プロパティ設定の名前空間の値が更新されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d0c89-161">Add the following code to the Program.cs or Module1.vb file, making sure to update the value of the namespace in the setting for the **SelectionNamespaces** property with the value you copied when you created the sample form.</span></span> 
    
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
            doc.setProperty("SelectionNamespaces","xmlns:my='https://schemas.microsoft.com/office/infopath/2003/myXSD/2006-09-06T23:17:34'");
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
          doc.setProperty("SelectionNamespaces", "xmlns:my='https://schemas.microsoft.com/office/infopath/2003/myXSD/2006-09-06T23:17:34'")
          ' Pre-populate the fields with specified values.
          doc.selectSingleNode("//my:FirstName").text = "My Name"
          doc.selectSingleNode("//my:LastName").text = "My LastName"
          doc.selectSingleNode("//my:Address").text = "My Address"
          ' Save the form, leaving InfoPath open.
          myXDoc.Save()
      End Sub
    End Module
    
   ```

4. <span data-ttu-id="d0c89-162">**[デバッグ]** メニューの **[デバッグの開始]** をクリックし、コンソール アプリケーションをコンパイルして実行します。</span><span class="sxs-lookup"><span data-stu-id="d0c89-162">On the **Debug** menu, click **Start Debugging** to compile and run the console application.</span></span> 
    
   <span data-ttu-id="d0c89-163">アプリケーションは Form1.xml として保存されているフォームを開き、"名"、"姓"、および "アドレス" の各フィールドにコードで指定された値を入力し、InfoPath を開いたまま、フォームを保存します。</span><span class="sxs-lookup"><span data-stu-id="d0c89-163">The application will open the form saved as Form1.xml and fill in the FirstName, LastName, and Address fields with the values specified in the code, and then save the form, leaving InfoPath open.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="d0c89-164">関連項目</span><span class="sxs-lookup"><span data-stu-id="d0c89-164">See also</span></span>

- [<span data-ttu-id="d0c89-165">Microsoft Office InfoPath プライマリ相互運用機能アセンブリについて</span><span class="sxs-lookup"><span data-stu-id="d0c89-165">About the Microsoft Office InfoPath Primary Interop Assembly</span></span>](about-the-microsoft-office-infopath-primary-interop-assembly.md)
- [<span data-ttu-id="d0c89-166">InfoPath XML 相互運用機能アセンブリについて</span><span class="sxs-lookup"><span data-stu-id="d0c89-166">About the InfoPath XML Interop Assembly</span></span>](about-the-infopath-xml-interop-assembly.md)

