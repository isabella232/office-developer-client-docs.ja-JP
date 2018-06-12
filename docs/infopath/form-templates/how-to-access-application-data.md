---
title: アプリケーション データにアクセス
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- application names [infopath 2007],accessing application name [InfoPath 2007],InfoPath 2007, accessing application data,accessing application version [InfoPath 2007],application versions [InfoPath 2007],language IDs [InfoPath 2007],LCID [InfoPath 2007],application data [InfoPath 2007],accessing language ID [InfoPath 2007]
localization_priority: Normal
ms.assetid: 2698d059-9955-4eec-85a6-79defb64e07e
description: InfoPath マネージ コード オブジェクト モデルには、InfoPath アプリケーションに関する情報 (フォームの基になる XML ドキュメント、フォーム定義ファイル (.xsf) などに関する情報) へのアクセスに使用できるオブジェクトとコレクションがあります。これらのデータには、InfoPath オブジェクト モデルの階層構造の最上位にあるオブジェクトを通じてアクセスします。このオブジェクトは、Application クラスを使用してインスタンス化されます。
ms.openlocfilehash: 3c3f6be4e90e292eb572da836bca0a8dcf1883cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799099"
---
# <a name="access-application-data"></a>アプリケーション データにアクセス

InfoPath マネージ コード オブジェクト モデルには、InfoPath アプリケーションに関する情報 (フォームの基になる XML ドキュメント、フォーム定義ファイル (.xsf) などに関する情報) へのアクセスに使用できるオブジェクトとコレクションがあります。これらのデータには、InfoPath オブジェクト モデルの階層構造の最上位にあるオブジェクトを通じてアクセスします。このオブジェクトは、[Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) クラスを使用してインスタンス化されます。 
  
Visual Studio 2012 を使用して作成した InfoPath マネージ コード フォーム テンプレート プロジェクトでは、 **this** (C#) または **Me** (Visual Basic) キーワードを使用して、現在の InfoPath アプリケーションを表す [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) クラスのインスタンスにアクセスできます。さらに、それを使用して、 [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) クラスのプロパティとメソッドにアクセスできます。 
  
## <a name="example"></a>例

### <a name="displaying-the-application-name-version-and-language-id"></a>アプリケーション名、バージョン、および言語 ID を表示する

次の例では、[Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Name.aspx) クラスの [Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Version.aspx) プロパティと [Version](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) プロパティを使用して、InfoPath の実行中のインスタンスの名前とバージョン番号を取得します。次に、 [LanguageSettings](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.LanguageSettings.aspx) プロパティを使用して **LanguageSettings** オブジェクトを取得し、そのオブジェクトを使用して、現在 InfoPath のユーザー インターフェイス言語に使われている言語の LCID (4 桁の数字) を取得します。最後に、これらすべての情報をメッセージ ボックスに表示します。 
  
> [!IMPORTANT]
> [!重要] **LanguageSettings** プロパティが機能するためには、(Visual Studio 2012 の [ **参照の追加**] ダイアログ ボックスの [ **COM**] タブから) Microsoft Office 14.0 オブジェクト ライブラリへの参照を確立する必要があります。これにより、 **LanguageSettings** クラスを含む **Microsoft.Office.Core** 名前空間への参照が確立されます。さらに、フォームは完全信頼として実行されている必要があります。 
  
この例を使用するには、フォーム コード モジュールの宣言セクションに **Microsoft.Office.Core** 名前空間の **using** または **Imports** ディレクティブが必要です。 
  
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


