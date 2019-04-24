---
title: Project Server ワークフロー開発の作業開始
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 735bbb04-a8c1-46c0-a346-42050f0ac9b1
description: project Server 2013 の需要管理プロセスには、プロジェクト提案およびポートフォリオ分析を管理するのに役立つワークフローが含まれています。 ここでは、Project Server のワークフローを作成する方法について説明します。
ms.openlocfilehash: 0a09022e63528f50ee4f0c8bd69bd6c34c5d8753
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344472"
---
# <a name="getting-started-developing-project-server-workflows"></a>Project Server ワークフロー開発の作業開始

project Server 2013 の需要管理プロセスには、プロジェクト提案およびポートフォリオ分析を管理するのに役立つワークフローが含まれています。 ここでは、Project Server のワークフローを作成する方法について説明します。
  
Project server 2013 ワークフローは、SharePoint server 2013 ワークフロープラットフォームを使用します。これは、Windows workflow Foundation (WF4) のバージョン4で構築されています。 WF4 ベースのワークフローは宣言型であり、ワークフローデザインツールがワークフローステージ、アクション、条件、およびその他の要素を XAML コードに保存することを意味します。これは、実行時に解釈されます。 宣言型ワークフローを作成するには、SharePoint Designer 2013 または Visual Studio 2012 のどちらかを使用できます。 ワークフローには、ワークフローマネージャークライアント1.0 実行エンジンが必要です。これは、オンプレミスのソリューションのローカルサーバー、または Project Online ソリューションのリモートサーバー上に存在することができます。
  
SharePoint Designer 2013 を使用して、比較的単純な宣言型ワークフローを作成できます。 複雑なワークフローおよび再利用できるワークフローテンプレートについては、Visual Studio 2012 を使用して Project Web App のワークフローを開発およびデバッグできます。 詳細については、「 [Visual Studio 2012 を使用してプロジェクトワークフローを作成する](https://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx)」を参照してください。
  
> [!IMPORTANT]
> ワークフローを開発およびテストするには、運用インストールではなく、Project Server のテストインストールを使用します。 Project Server 2013 のプレリリース版用に開発されたワークフローは、リリースバージョンをテストする必要があり、再度作成して再展開する必要がある場合があります。 
  
## <a name="in-this-section"></a>このセクションの内容

[需要管理用の Project Server ワークフローを作成する](create-a-project-server-workflow-for-demand-management.md)
  
## <a name="see-also"></a>関連項目



[ユーザー設定フィールドを一括更新し、project Online ワークフローからプロジェクトサイトを作成する](bulk-update-custom-fields-and-create-project-sites-from-workflow-in-project.md)


[SharePoint Designer 2013 および Visio 2013 でのワークフロー開発](https://msdn.microsoft.com/library/jj163272%28office.15%29.aspx)
  
[SharePoint ワークフローの新機能](https://msdn.microsoft.com/library/jj163177.aspx)
  
[Visual Studio を使用した SharePoint 2013 ワークフローの開発](https://msdn.microsoft.com/library/jj163199.aspx)
  
[Visual Studio 2012 を使用してプロジェクトワークフローを作成する](https://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx)
  
[Windows Workflow Foundation](https://msdn.microsoft.com/library/dd489441.aspx)
  
[開発者による .net 4 での Windows Workflow Foundation (WF) の概要](https://msdn.microsoft.com/library/ee342461.aspx)
  
[オンデマンド管理のためのガイド (ホワイトペーパー)](https://msdn.microsoft.com/library/ff973112.aspx)

