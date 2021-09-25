---
title: Project クライアントのプログラミング
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
f1_keywords:
- object model
- Project object model
- Project VBA
- VBA
keywords:
- vba、プロジェクト オブジェクト モデル、Project、プログラミング性、Project VBA、Visual Basic for Applications、Project オブジェクト モデル、VBA、オブジェクト モデル、VBA、Visual Basic for Applications
ms.localizationpriority: medium
ms.assetid: 0ad49ff6-8dff-4379-a52c-d292c53c2bc0
description: Project 2013 デスクトップ クライアント アプリケーション (Project Standard 2013 および Project Professional 2013) は、VBA を使用してマクロを記述することでカスタマイズおよび拡張できます。 2012 Visual Studioを使用して、リボン のユーザー インターフェイスをカスタマイズし、複雑なアドインを作成できます。Officeアドインを使用すると、2013 年の一般的なプラットフォーム上に構築Project作業ウィンドウの新しい機能拡張モデルをOfficeできます。 Project Standard 2013 および Project Professional 2013 では、一般的な Office アドインを実行し、Project 用に特別に開発された作業ウィンドウ アドインを使用して、SharePoint、他の Web サイトや Web アプリケーション、および外部データと統合できます。
ms.openlocfilehash: 952646dd27310b2fe2e999d87474055a76045c45
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629019"
---
# <a name="project-client-programming"></a>Project クライアントのプログラミング

Project 2013 デスクトップ クライアント アプリケーション (Project Standard 2013 および Project Professional 2013) は、VBA を使用してマクロを記述することでカスタマイズおよび拡張できます。 2012 Visual Studioを使用して、リボン のユーザー インターフェイスをカスタマイズし、複雑なアドインを作成できます。Officeアドインを使用すると、2013 年の一般的なプラットフォーム上に構築Project作業ウィンドウの新しい機能拡張モデルをOfficeできます。 Project Standard 2013 および Project Professional 2013 では、一般的な Office アドインを実行し、Project 用に特別に開発された作業ウィンドウ アドインを使用して、SharePoint、他の Web サイトや Web アプリケーション、および外部データと統合できます。
  
 **ファイルへのVisual Studio** VBA は、マクロを記録し、比較的単純なオートメーション ソリューションを開発する場合に役立ちます。 作業ウィンドウ アドイン、アドイン、およびより複雑で安全で拡張性が高く、展開しやすいソリューションを開発するには、Visual Studio 2012 を使用することをお勧めします。 Microsoft .NET Framework 4.0 および Project 2013 プライマリ相互運用機能アセンブリは、Project 2013 デスクトップ クライアントを自動化および統合するソリューションの開発と展開に多くの利点を提供します。 
  
> [!NOTE]
> 2010 Visual Studioを使用して、Projectを開発できます。ただし、Visual Studio 2012 には、アドイン クライアントを作成するように設計Office拡張機能が含まれています。 
  
2013 年 2013 年の VBA の Project **MSProject** オブジェクト モデルは、基本的に **Microsoft.Office と同じです。Interop.MSProject** オブジェクト モデルは、Office 開発者向けツール (Visual Studio 2013 とも呼ばれる) を使用したマネージ コード ソリューションVSTO。 Visual Studio 2012 には、Project 2010 および Project 2013 (Project Standard バージョンまたは Project Professional バージョン) 用のアプリケーション レベル アドインを開発するためのテンプレートが含まれています。 VSTO および Office Developer Tools for Visual Studio 2012 は、Project デスクトップ クライアントおよび他の Office 2013 アプリケーションを使用し、SharePoint サイト、リスト、およびワークフローと統合できる高度な統合ソリューションの開発、テスト、展開を簡素化します。 
  
Office と SharePoint の作業ウィンドウ アドインおよび他のアドインは、Project Online とオンプレミスの両方のインストールで使用するために、Office ストア (参照) で販売できます。 [https://office.microsoft.com/store/](https://office.microsoft.com/en-us/store/) VBA マクロVSTOアドインは、Office ストアにOfficeできません。これらは、ローカルで使用するために設計され、Project StandardとProject Professional。 VBA マクロは、プロジェクト内で配布できます。MPP ファイル、コンピューターの Global.MPT ファイルにインストールするか、またはサーバー 2013 のエンタープライズ グローバル テンプレートに配布Projectします。 VSTO展開を通じて、より安全にアドインを配布ClickOnce更新が[](https://msdn.microsoft.com/library/t71a733d.aspx)容易になります。 
  
## <a name="reference"></a>リファレンス

[Project VBA 開発者向けリファレンス](https://msdn.microsoft.com/library/ee861523%28office.15%29.aspx)入門および VBA のヘルプ記事が含まれる。 
  
## <a name="related-sections"></a>関連情報

[Project Server 2013 アーキテクチャ](project-server-2013-architecture.md)クライアントがサーバーとProjectする方法をProjectします。 
  
## <a name="see-also"></a>関連項目

- [開発者向け Project](https://msdn.microsoft.com/office/aa905469)
- [Officeデベロッパー センター](https://dev.office.com)
- [Visual Studioデベロッパー センター](https://msdn.microsoft.com/vstudio/aa718325.aspx)
- [ClickOnceセキュリティと展開](https://msdn.microsoft.com/library/t71a733d.aspx)
- [利用可能なフィールド リファレンス](https://support.office.com/en-us/article/available-fields-reference-615a4563-1cc3-40f4-b66f-1b17e793a460)

