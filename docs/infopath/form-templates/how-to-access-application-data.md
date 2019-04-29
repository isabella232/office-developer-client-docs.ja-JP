---
title: アプリケーション データにアクセスする方法
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- application names [infopath 2007],accessing application name [InfoPath 2007],InfoPath 2007, accessing application data,accessing application version [InfoPath 2007],application versions [InfoPath 2007],language IDs [InfoPath 2007],LCID [InfoPath 2007],application data [InfoPath 2007],accessing language ID [InfoPath 2007]
localization_priority: Normal
ms.assetid: 2698d059-9955-4eec-85a6-79defb64e07e
description: InfoPath マネージ コード オブジェクト モデルには、InfoPath アプリケーションに関する情報 (フォームの基になる XML ドキュメント、フォーム定義ファイル (.xsf) などに関する情報) へのアクセスに使用できるオブジェクトとコレクションがあります。これらのデータには、InfoPath オブジェクト モデルの階層構造の最上位にあるオブジェクトを通じてアクセスします。このオブジェクトは、Application クラスを使用してインスタンス化されます。
ms.openlocfilehash: 8da72313807584ee599d65701d009786dd631979
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417232"
---
# <a name="access-application-data"></a><span data-ttu-id="4babb-105">アプリケーション データにアクセスする方法</span><span class="sxs-lookup"><span data-stu-id="4babb-105">Access Application Data</span></span>

<span data-ttu-id="4babb-p102">InfoPath マネージ コード オブジェクト モデルには、InfoPath アプリケーションに関する情報 (フォームの基になる XML ドキュメント、フォーム定義ファイル (.xsf) などに関する情報) へのアクセスに使用できるオブジェクトとコレクションがあります。これらのデータには、InfoPath オブジェクト モデルの階層構造の最上位にあるオブジェクトを通じてアクセスします。このオブジェクトは、[Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) クラスを使用してインスタンス化されます。</span><span class="sxs-lookup"><span data-stu-id="4babb-p102">The InfoPath managed code object model provides objects and collections that can be used to gain access to information about the InfoPath application, including information related to a form's underlying XML document and the form definition (.xsf) file. This data is accessed through the top-level object in the InfoPath object model hierarchy, which is instantiated by using the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class.</span></span> 
  
<span data-ttu-id="4babb-108">Visual Studio 2012 を使用して作成した InfoPath マネージ コード フォーム テンプレート プロジェクトでは、 **this** (C#) または **Me** (Visual Basic) キーワードを使用して、現在の InfoPath アプリケーションを表す [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) クラスのインスタンスにアクセスできます。さらに、それを使用して、 [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) クラスのプロパティとメソッドにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="4babb-108">In an InfoPath managed code form template project created using Visual Studio 2012, you can use the **this** (C#) or **Me** (Visual Basic) keyword to access an instance of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class that represents the current InfoPath application, which can then be used to access the properties and methods of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class.</span></span> 
  
## <a name="example"></a><span data-ttu-id="4babb-109">例</span><span class="sxs-lookup"><span data-stu-id="4babb-109">Example</span></span>

### <a name="displaying-the-application-name-version-and-language-id"></a><span data-ttu-id="4babb-110">アプリケーション名、バージョン、および言語 ID を表示する</span><span class="sxs-lookup"><span data-stu-id="4babb-110">Displaying the Application Name, Version, and Language ID</span></span>

<span data-ttu-id="4babb-p103">次の例では、[Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Name.aspx) クラスの [Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Version.aspx) プロパティと [Version](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) プロパティを使用して、InfoPath の実行中のインスタンスの名前とバージョン番号を取得します。次に、 [LanguageSettings](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.LanguageSettings.aspx) プロパティを使用して **LanguageSettings** オブジェクトを取得し、そのオブジェクトを使用して、現在 InfoPath のユーザー インターフェイス言語に使われている言語の LCID (4 桁の数字) を取得します。最後に、これらすべての情報をメッセージ ボックスに表示します。</span><span class="sxs-lookup"><span data-stu-id="4babb-p103">In the following example, the [Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Name.aspx) and [Version](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Version.aspx) properties of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class are used to return the name and version number of the running instance of InfoPath. The [LanguageSettings](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.LanguageSettings.aspx) property is then used to return a **LanguageSettings** object, which in turn is used to return the LCID (a four-digit number) for the language that is currently being used for the InfoPath user interface language. Finally, all of this information is displayed in a message box.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="4babb-p104">**LanguageSettings** プロパティが機能するためには、(Visual Studio 2012 の [ **参照の追加**] ダイアログ ボックスの [ **COM**] タブから) Microsoft Office 14.0 オブジェクト ライブラリへの参照を確立する必要があります。これにより、 **LanguageSettings** クラスを含む **Microsoft.Office.Core** 名前空間への参照が確立されます。さらに、フォームは完全信頼として実行されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="4babb-p104">For the **LanguageSettings** property to work, you must establish a reference to the Microsoft Office 14.0 Object Library from the **COM** tab of the **Add Reference** dialog box in Visual Studio 2012. This will establish a reference to the **Microsoft.Office.Core** namespace, which contains the **LanguageSettings** class. Additionally, the form must be running as Full Trust.</span></span> 
  
<span data-ttu-id="4babb-117">この例を使用するには、フォーム コード モジュールの宣言セクションに **Microsoft.Office.Core** 名前空間の **using** または **Imports** ディレクティブが必要です。</span><span class="sxs-lookup"><span data-stu-id="4babb-117">This example requires a **using** or **Imports** directive for the **Microsoft.Office.Core** namespace in the declarations section of the form code module.</span></span> 
  
```cs
string appName = this.Application.Name;
string appVersion = this.Application.Version;
LanguageSettings langSettings = 
   (LanguageSettings)this.Application.LanguageSettings;
int langID = 
   langSettings.get_LanguageID(MsoAppLanaguageID.msoLanguageIDUI);
MessageBox.Show(
   "Name: " + appName + System.Environment.NewLine +
   "Version: " + appVersion + System.Environment.NewLine +
   "Language ID: " + langID);
```

```vb
Dim appName As String appName = Me.Application.Name
Dim appVersion As String = Me.Application.Version
Dim langSettings As LanguageSettings = _
   DirectCast(Me.Application.LanguageSettings, LanguageSettings)
Dim langID As Integer = _
   langSettings.LanguageID(MsoAppLanaguageID.msoLanguageIDUI)
MessageBox.Show( _
   "Name: " + appName + System.Environment.NewLine + _
   "Version: " + appVersion + System.Environment.NewLine + _
   "Language ID: " + langID)
```


