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
ms.openlocfilehash: af8bfbb0322b9d70fb85ba21a757a581ba423a44
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383164"
---
# <a name="external-automation-scenarios-and-examples"></a>外部オートメーションのシナリオと例

Microsoft Office InfoPath プライマリ相互運用機能アセンブリ (Microsoft.Office.Interop.InfoPath.dll) と InfoPath XML 相互運用機能アセンブリ (Microsoft.Office.Interop.InfoPath.Xml.dll) が提供するメンバーは、InfoPath を自動化するためのマネージ コードの記述をサポートします。 
  
## <a name="establishing-references-to-the-microsoft-office-infopath-primary-interop-and-infopath-xml-interop-assemblies"></a>Microsoft Office InfoPath プライマリ相互運用機能と InfoPath XML 相互運用機能アセンブリへの参照を確立します。

InfoPath を自動化するためのマネージ コードを記述するには、Microsoft InfoPath のプライマリ相互運用機能と、InfoPath XML 相互運用機能アセンブリへの参照を確立する必要があります。 Microsoft InfoPath のプライマリ相互運用機能アセンブリは、IPEDITOR によって公開される COM オブジェクト モデルとの相互運用性のサポートを提供します。[Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx)名前空間のメンバーを使用して DLL があります。 InfoPath XML 相互運用機能アセンブリは、 [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml)名前空間のメンバーを使用して、「Microsoft XML Core Services (MSXML) で公開されている COM オブジェクト モデルとの相互運用性のサポートを提供します。 
  
> [!IMPORTANT]
> InfoPath を自動化するマネージ コード アプリケーションのユーザーは、InfoPath、Microsoft Office InfoPath のプライマリ相互運用機能アセンブリ、および自分のコンピューターにインストールされている InfoPath XML 相互運用機能アセンブリが必要です。 InfoPath セットアップ プログラムで [ **.NET プログラミング サポート**] オプションは、InfoPath の標準的なインストールのため、**マイ コンピューターから実行**に設定されます。
>  
> その結果、または.NET Framework 1.1 再配布可能な.NET Framework 1.1 ソフトウェア開発キット (SDK)、またはそれ以降がインストールされている、これらの相互運用機能アセンブリが既定でもインストールされます。 これらの相互運用機能アセンブリがユーザーのコンピューターで利用できない場合は、する必要があることを確認して、.NET Framework 1.1 以降がインストールされているセットアップを変更し、.NET プログラミングの**を設定する**コントロール パネル**から**プログラムと機能**を実行サポート**InfoPath で **[マイ コンピューターから実行**するためのオプションです。 
  
次の手順では、Visual Studio プロジェクトに Microsoft Office InfoPath プライマリ相互運用機能アセンブリと InfoPath XML 相互運用機能アセンブリの参照を設定する方法について説明します。
  
Microsoft.Office.Interop.InfoPath プライマリ相互運用機能アセンブリの参照を設定するには、**[参照の追加]** ダイアログ ボックスの **[COM]** タブ上で **Microsoft InfoPath 3.0 タイプ ライブラリ**の参照を設定します。**[COM]** タブから参照を設定するものの、InfoPath セットアップ プログラムがグローバル アセンブリ キャッシュ (GAC) にインストールした Microsoft.Office.Interop.InfoPath.dll プライマリ相互運用機能アセンブリへの参照が確立されます。 
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopath-primary-interop-assembly"></a>Microsoft.Office.Interop.InfoPath プライマリ相互運用機能アセンブリへの参照を設定する

1. Visual Studio のマネージ コード プロジェクトを開きます。
    
2. **ソリューション エクスプローラー**で [**参照**] を右クリックし、[**参照の追加**] をクリックします。
    
3. **[COM]** タブの **[Microsoft InfoPath 3.0 タイプ ライブラリ]** をダブルクリックし、**[OK]** をクリックします。
    
Microsoft.Office.Interop.InfoPath.Xml の相互運用機能アセンブリへの参照を設定するには、<_ドライブ_> に既定でインストールされている Microsoft.Office.Interop.InfoPath.Xml.dll ファイルを参照: \Program Files\Microsoft Office\OFFICE14 フォルダー. 場合でも、アセンブリのコピーをローカル ファイル システムに指定すると、この手順は、グローバル アセンブリ キャッシュ (GAC) に InfoPath セットアップ プログラムによってインストールされる Microsoft.Office.Interop.InfoPath.Xml.dll のアセンブリへの参照を確立します。
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopathxml-interop-assembly"></a>Microsoft.Office.Interop.InfoPath Xml 相互運用機能アセンブリへの参照を設定する

1. **コンソール アプリケーション**または **Windows アプリケーション**などの Visual Studio マネージ コード プロジェクトを開くか、作成します。
    
2. **ソリューション エクスプ ローラー**では、**参照**のを右クリックし、 **[参照の追加**] をクリックします。
    
3. [ **.NET** ] タブの [**参照**] をクリックします、<_ドライブ_> に移動: \Program Files\Microsoft Office\OFFICE14 フォルダーでは、[Microsoft.Office.Interop.InfoPath.Xml.dll] をクリックします。
    
4. **[OK]** をクリックします。
    
## <a name="automate-changing-the-value-of-a-field"></a>フィールドの値の変更を自動化します。

InfoPath の売上報告書フォーム テンプレートのユーザーの顧客企業の 1 社が「Company A」から「Company B」に自社名を先日変更したとします。開発者は、このフォーム テンプレートから保存された売上報告書フォームを自動的に更新して社名変更を反映するコードを記述するように依頼されました。次のシナリオでは、[customerName] フィールドにバインドされたテキスト ボックスを含むフォームを想定します。
  
### <a name="create-the-sample-form-template-and-form"></a>サンプル フォーム テンプレートおよびフォームを作成する

1. InfoPath を開き、空白のフォーム テンプレートを作成します。
    
2. フォームに**テキスト ボックス**コントロールを追加し、コントロール様にバインドされているフィールド名を入力します。
    
3. **[フィールド]** タスク ウィンドウの **[マイフィールド]** フォルダーを右クリックし、**[プロパティ]** をクリックします。
    
4. **[詳細]** タブから、次の値の **[名前空間:]** に続く値を選択してコピーし、これをメモ帳または取得できる他の場所に貼り付けます。この値は、コード内の **SelectionNamespaces** プロパティの値を設定する時に必要になります。 
    
5. C:\Test という名前のフォルダーにフォーム テンプレートを発行し、「Template1」という既定の名前とします。 
    
6. フォーム テンプレートを開き、[customerName] フィールドにバインドされているテキストボックスに「Company A」を入力し、フォームを「Form1」として保存します。 
    
### <a name="create-a-managed-code-console-application-to-change-the-name-from-company-a-to-company-b"></a>企業名を「Company A」から「Company B」変更するマネージ コード コンソール アプリケーションを作成します。

1. Visual Studio を開き、[UpdateCustomer]という名前で新しい Visual C# または Visual Basic コンソール アプリケーションを作成します。
    
2. 前述のように、Microsoft Office InfoPath プライマリ相互運用機能アセンブリおよび InfoPath XML 相互運用機能アセンブリのへ参照を確立します。
    
3. 次のコードを Program.cs または Module1.vb ファイルに追加し、サンプル フォームを作成したときにコピーした値に、**SelectionNamespaces** プロパティ設定の名前空間の値が更新されることを確認します。 
    
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

4. **[デバッグ]** メニューの **[デバッグの開始]** をクリックし、コンソール アプリケーションをコンパイルして実行します。 
    
   アプリケーションは Form1.xml として保存されているフォームを開き、「Company A」という値を含むすべての customerName 要素をループし、その値を「Company B」に変更します。操作が完了すると、フォームの新しいコピーが C:\Test フォルダーに Form2.xml として保存されます。 
    
## <a name="automate-opening-a-form-and-populating-field-values"></a>フォームを開くと、フィールドの値を設定を自動化します。

次の例では、空白のフォームを開き、フォームの名、姓、アドレスの各フィールドを設定する操作を自動で行います。このシナリオでは、“名”、“姓”、“アドレス” という名前の各フィールドにバインドされた 3 つのテキスト ボックスを含むフォームを想定します。
  
### <a name="create-the-sample-form-template-and-form"></a>サンプル フォーム テンプレートおよびフォームを作成する

1. InfoPath を開き、空白のフォームを作成します。
    
2. テキスト ボックス コントロールを 3 つ追加し、コントロールにバインドされたフィールドの名前を“名”、“姓”、“アドレス” にします。必要なその他のフィールドを追加します。
    
3. **[フィールド]** タスク ウィンドウの **[マイフィールド]** フォルダーを右クリックし、**[プロパティ]** をクリックします。
    
4. **[詳細]** タブから、次の値の **[名前空間:]** に続く値を選択してコピーし、これをメモ帳または取得できる他の場所に貼り付けます。この値は、コード内の **SelectionNamespaces** プロパティの値を設定する時に必要になります。 
    
5. C:\Test という名前のフォルダーにフォーム テンプレートを発行し、「Template1」という既定の名前とします。
    
6. フォーム テンプレートを開き、空白のフォームを C:\Temp に「Form1」として保存します。
    
### <a name="create-a-managed-code-console-application-to-open-the-form-and-populate-the-fields"></a>マネージ コード コンソール アプリケーションを作成し、フォームを開いてフィールドを設定します。

1. Visual Studio を開き、「OpenForm」という名前で新しい Visual C# または Visual Basic コンソール アプリケーションを作成します。
    
2. 前述のように、Microsoft Office InfoPath プライマリ相互運用機能アセンブリおよび InfoPath XML 相互運用機能アセンブリのへ参照を確立します。
    
3. 次のコードを Program.cs または Module1.vb ファイルに追加し、サンプル フォームを作成したときにコピーした値に、**SelectionNamespaces** プロパティ設定の名前空間の値が更新されることを確認します。 
    
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

4. **[デバッグ]** メニューの **[デバッグの開始]** をクリックし、コンソール アプリケーションをコンパイルして実行します。 
    
   アプリケーションは Form1.xml として保存されているフォームを開き、"名"、"姓"、および "アドレス" の各フィールドにコードで指定された値を入力し、InfoPath を開いたまま、フォームを保存します。 
    
## <a name="see-also"></a>関連項目

- [Microsoft Office InfoPath プライマリ相互運用機能アセンブリについて](about-the-microsoft-office-infopath-primary-interop-assembly.md)
- [InfoPath XML 相互運用機能アセンブリについて](about-the-infopath-xml-interop-assembly.md)

