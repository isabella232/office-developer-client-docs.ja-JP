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
- vba、project オブジェクトモデル、プロジェクト、プログラミング、プログラミング、プロジェクト VBA、Visual Basic for applications、project オブジェクトモデル、VBA、オブジェクトモデル、VBA、Visual basic for applications
localization_priority: Normal
ms.assetid: 0ad49ff6-8dff-4379-a52c-d292c53c2bc0
description: project 2013 デスクトップクライアントアプリケーション (project Standard 2013 および project Professional 2013) は、VBA を使用してマクロを作成することでカスタマイズおよび拡張することができます。 Visual Studio 2012 を使用して、リボンユーザーインターフェイスをカスタマイズしたり、複雑なアドインを作成したりできます。 office アドインでは、共通の office 2013 プラットフォーム上に構築されたプロジェクト内の作業ウィンドウの新しい拡張モデルが有効になります。 project Standard 2013 および project Professional 2013 は、一般的な Office アドインを実行し、project 用に特に開発された作業ウィンドウアドインを使用して SharePoint、他の web アプリケーション、および外部データと統合することができます。
ms.openlocfilehash: cc345f0ff91dfb573dd86c256e89df478edd4924
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301513"
---
# <a name="project-client-programming"></a>Project クライアントのプログラミング

project 2013 デスクトップクライアントアプリケーション (project Standard 2013 および project Professional 2013) は、VBA を使用してマクロを作成することでカスタマイズおよび拡張することができます。 Visual Studio 2012 を使用して、リボンユーザーインターフェイスをカスタマイズしたり、複雑なアドインを作成したりできます。 office アドインでは、共通の office 2013 プラットフォーム上に構築されたプロジェクト内の作業ウィンドウの新しい拡張モデルが有効になります。 project Standard 2013 および project Professional 2013 は、一般的な Office アドインを実行し、project 用に特に開発された作業ウィンドウアドインを使用して SharePoint、他の web アプリケーション、および外部データと統合することができます。
  
 **Visual Studio への移行**VBA は、マクロを記録し、比較的単純な自動化ソリューションを開発するのに便利です。 作業ウィンドウアドイン、アドイン、およびより複雑で安全でスケーラブルなソリューションを開発するには、Visual Studio 2012 を使用することをお勧めします。 Microsoft .net Framework 4.0 および project 2013 プライマリ相互運用機能アセンブリは、project 2013 デスクトップクライアントを自動化および統合するソリューションを開発および展開するための多くの利点を提供します。 
  
> [!NOTE]
> Visual Studio 2010 を使用して、プロジェクトアドインを開発できます。ただし、Visual Studio 2012 には、Office アドインクライアントを作成するために設計されたテンプレートと拡張機能が含まれています。 
  
project 2013 の**msproject**オブジェクトモデルは、office Developer Tools for Visual Studio 2013 (VSTO とも呼ばれます) を使用したマネージコードソリューションのための、基本的には、「 **Microsoft office**と同じ」の msproject オブジェクトモデルです。 Visual Studio 2012 には、project 2010 および project 2013 (project Standard または project Professional バージョン) 用のアプリケーションレベルのアドインを開発するためのテンプレートが含まれています。 VSTO および Office Developer Tools for Visual Studio 2012 は、プロジェクトデスクトップクライアントおよびその他の office 2013 アプリケーションを使用して、SharePoint サイト、リスト、およびを統合できる高度な統合ソリューションの開発、テスト、および展開を簡素化します。ワークフロー. 
  
作業ウィンドウアドインと office および SharePoint 用の他のアドインは、office ストアで販売できます (「」 [https://office.microsoft.com/store/](https://office.microsoft.com/en-us/store/)を参照)、Project Online とオンプレミスの両方のインストールで使用できます。 VBA マクロと VSTO アドインを Office ストアに配布することはできません。project Standard および project Professional でローカルに使用するように設計されています。 プロジェクト内で VBA マクロを配布できます。MPP ファイルをコンピューター上の global.mpt ファイルにインストールするか、Project Server 2013 のエンタープライズグローバルテンプレートに配布します。 VSTO アドインは[ClickOnce](https://msdn.microsoft.com/library/t71a733d.aspx)展開により安全に配布できます。これにより、簡単に更新できるようになります。 
  
## <a name="reference"></a>リファレンス

[Project VBA 開発者用リファレンス](https://msdn.microsoft.com/library/ee861523%28office.15%29.aspx)紹介と VBA のヘルプ記事が含まれています。 
  
## <a name="related-sections"></a>関連情報

[Project Server 2013 アーキテクチャ](project-server-2013-architecture.md)project クライアントが project Server と対話する方法を示します。 
  
## <a name="see-also"></a>関連項目

- [開発者向け Project](https://msdn.microsoft.com/office/aa905469)
- [Office デベロッパーセンター](https://dev.office.com)
- [Visual Studio デベロッパーセンター](https://msdn.microsoft.com/vstudio/aa718325.aspx)
- [ClickOnce のセキュリティと展開](https://msdn.microsoft.com/library/t71a733d.aspx)
- [利用可能なフィールド リファレンス](https://support.office.com/en-us/article/available-fields-reference-615a4563-1cc3-40f4-b66f-1b17e793a460)

