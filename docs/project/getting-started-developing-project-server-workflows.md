---
title: Project Server ワークフロー開発の作業開始
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 735bbb04-a8c1-46c0-a346-42050f0ac9b1
description: Project Server 2013 の需要管理プロセスには、プロジェクト提案とポートフォリオ分析の管理に役立つワークフローが含まれます。 ここでは、Project Server のワークフローを作成する方法について説明します。
ms.openlocfilehash: 0a09022e63528f50ee4f0c8bd69bd6c34c5d8753
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344472"
---
# <a name="getting-started-developing-project-server-workflows"></a>Project Server ワークフロー開発の作業開始

Project Server 2013 の需要管理プロセスには、プロジェクト提案とポートフォリオ分析の管理に役立つワークフローが含まれます。 ここでは、Project Server のワークフローを作成する方法について説明します。
  
ProjectServer 2013 ワークフローでは、SharePoint Server 2013 ワークフロー プラットフォームを使用します。これは、Windows ワークフローファンデーション (WF4) のバージョン 4 で構築されています。 WF4 ベースのワークフローは宣言型であり、ワークフロー設計ツールはワークフロー ステージ、アクション、条件、その他の要素を XAML コードに保存し、実行時に解釈されます。 宣言型ワークフローを作成SharePointデザイナー 2013 または 2012 Visual Studioを使用できます。 ワークフローには、ワークフロー マネージャー クライアント 1.0 実行エンジンが必要です。これは、オンプレミス ソリューションのローカル サーバー上に、または Project Online ソリューション用のリモート サーバー上にある場合があります。
  
デザイナー 2013 SharePoint使用して、比較的単純な宣言型ワークフローを作成できます。 複雑なワークフローと再利用できるワークフロー テンプレートの場合は、Visual Studio 2012 を使用して、Project Web App のワークフローを開発およびデバッグできます。 詳細については[、「2012 年 2012 年を使用Projectワークフローの作成Visual Studio参照してください](https://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx)。
  
> [!IMPORTANT]
> ワークフローを開発およびテストするには、Projectサーバーのテスト インストールを使用します。 Project Server 2013 のプレリリース バージョン用に開発されたワークフローは、リリース バージョンについてテストする必要があります。また、再度作成して再展開する必要があります。 
  
## <a name="in-this-section"></a>このセクションの内容

[需要管理Projectサーバー ワークフローを作成する](create-a-project-server-workflow-for-demand-management.md)
  
## <a name="see-also"></a>関連項目



[カスタム フィールドを一括更新し、プロジェクト サイトをワークフローからProject Onlineする](bulk-update-custom-fields-and-create-project-sites-from-workflow-in-project.md)


[SharePoint Designer 2013 および Visio 2013 でのワークフロー開発](https://msdn.microsoft.com/library/jj163272%28office.15%29.aspx)
  
[SharePoint ワークフローの新機能](https://msdn.microsoft.com/library/jj163177.aspx)
  
[Visual Studio を使用した SharePoint 2013 ワークフローの開発](https://msdn.microsoft.com/library/jj163199.aspx)
  
[2012 Projectを使用したワークフロー Visual Studio作成](https://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx)
  
[Windows Workflow Foundation](https://msdn.microsoft.com/library/dd489441.aspx)
  
[開発者による .NET 4 Windowsワークフローファンデーション (WF) の概要](https://msdn.microsoft.com/library/ee342461.aspx)
  
[Hitchhiker の需要管理ガイド (ホワイト ペーパー)](https://msdn.microsoft.com/library/ff973112.aspx)

