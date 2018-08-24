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
- vba プロジェクト オブジェクト モデルでは、プロジェクト、プログラム、プログラミング、VBA のプロジェクトを Visual Basic for Applications プロジェクト オブジェクト モデルでは、VBA オブジェクト モデル、VBA では、Visual Basic for Applications
localization_priority: Normal
ms.assetid: 0ad49ff6-8dff-4379-a52c-d292c53c2bc0
description: Project 2013 のデスクトップ クライアント アプリケーション-標準 2013 のプロジェクトとプロジェクトの評価のため、カスタマイズし、マクロを作成するのには VBA を使用して拡張できます。 Visual Studio 2012 を使用するにはリボンのユーザー インターフェイスをカスタマイズし、新しい機能拡張モデルの一般的な Office 2013 のプラットフォームに組み込まれているプロジェクトでの作業ウィンドウに Office アドインを有効に複雑なアドインを作成します。 プロジェクト標準 2013 および評価のためのプロジェクトは一般的な Office のアドインを実行し、アドインを使用して作業ウィンドウの SharePoint、他の web サイトや web アプリケーション、および外部のデータと統合するプロジェクト専用に開発されました。
ms.openlocfilehash: 9e89c5a1f6486ce49ad8b95bcd7a92497b7a2436
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594741"
---
# <a name="project-client-programming"></a>Project クライアントのプログラミング

Project 2013 のデスクトップ クライアント アプリケーション-標準 2013 のプロジェクトとプロジェクトの評価のため、カスタマイズし、マクロを作成するのには VBA を使用して拡張できます。 Visual Studio 2012 を使用するにはリボンのユーザー インターフェイスをカスタマイズし、新しい機能拡張モデルの一般的な Office 2013 のプラットフォームに組み込まれているプロジェクトでの作業ウィンドウに Office アドインを有効に複雑なアドインを作成します。 プロジェクト標準 2013 および評価のためのプロジェクトは一般的な Office のアドインを実行し、アドインを使用して作業ウィンドウの SharePoint、他の web サイトや web アプリケーション、および外部のデータと統合するプロジェクト専用に開発されました。
  
 **Visual Studio への移動**VBA では、マクロを記録し、比較的単純なオートメーション ソリューションを開発するのに便利です。 作業ウィンドウ - アドインを開発するには、アドインと複雑なセキュリティで保護された、スケーラブルで、ますます簡単に配置したソリューションをお勧め Visual Studio 2012 を使用することです。 Microsoft.NET Framework 4.0 および Project 2013 のプライマリ相互運用機能アセンブリは、開発および展開を自動化し、Project 2013 のデスクトップ クライアントを統合するソリューションの多くの利点を提供します。 
  
> [!NOTE]
> プロジェクトのアドインを開発するのには、Visual Studio 2010 を使用できます。ただし、Visual Studio 2012 には、テンプレートとクライアントの Office アドインを作成するように設計された拡張機能が含まれています。 
  
**MSProject** Project 2013 での VBA オブジェクト モデルは、基本的に 2013 (VSTO とも呼ばれます) を Visual Studio の Office 開発ツールにマネージ コード ソリューションの**Microsoft.Office.Interop.MSProject**オブジェクト モデルと同じです。 Visual Studio 2012 には、アプリケーション レベルのアドイン プロジェクト 2010年と Project 2013 (標準的なプロジェクトまたはプロジェクトのプロフェッショナル ・ バージョン) を開発するためのテンプレートが含まれています。 VSTO と Visual Studio 2012 ののための Office 開発ツールが簡単に開発、テスト、および Project デスクトップ クライアントおよびその他の Office 2013 アプリケーションを使用でき、SharePoint サイト、リスト、統合の高度な統合ソリューションを展開してワークフローです。 
  
作業ウィンドウ - アドインおよびその他のアドインを Office および SharePoint は、Office ストアで販売できます (を参照してください[http://office.microsoft.com/store/](http://office.microsoft.com/en-us/store/)) プロジェクトのオンラインと設置型の両方のインストールで使用するためです。 Office ストアには、マクロを VBA と VSTO アドインを配布することはできません。標準的なプロジェクトと Project Professional をローカルで使用するためのものです。 プロジェクト内の VBA マクロを配布することができます。MPP ファイルは、Global.MPT ファイル、お使いのコンピューター上でインストールまたは Project Server 2013 のエンタープライズ グローバル テンプレートの配布。 VSTO アドインは、 [ClickOnce](http://msdn.microsoft.com/en-us/library/t71a733d.aspx)配置では、簡単に更新プログラムを有効より安全に配布できます。 
  
## <a name="reference"></a>リファレンス

[プロジェクトの VBA の開発者用リファレンス](http://msdn.microsoft.com/en-us/library/ee861523%28office.15%29.aspx)入門が含まれていて、VBA ヘルプの記事です。 
  
## <a name="related-sections"></a>関連情報

[Project Server 2013 のアーキテクチャ](project-server-2013-architecture.md)クライアント プロジェクトが Project Server とどのようにやり取りする方法を示しています。 
  
## <a name="see-also"></a>関連項目

- [開発者のためのプロジェクト](http://msdn.microsoft.com/en-us/office/aa905469)
- [Office デベロッパー センター](https://dev.office.com)
- [Visual Studio のデベロッパー センター](http://msdn.microsoft.com/en-us/vstudio/aa718325.aspx)
- [ClickOnce のセキュリティと展開](http://msdn.microsoft.com/en-us/library/t71a733d.aspx)
- [利用可能なフィールドの参照](https://support.office.com/en-us/article/available-fields-reference-615a4563-1cc3-40f4-b66f-1b17e793a460)

