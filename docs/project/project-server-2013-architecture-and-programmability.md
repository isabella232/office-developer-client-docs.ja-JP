---
title: Project Server 2013 のアーキテクチャおよびプログラミング
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
f1_keywords:
- architecture
- platform
- Project
- Project architecture
- Project programmability
- Project Server architecture
- Project Server programmability
keywords:
- project 2013、アーキテクチャとプログラミング、プログラミング、Project Server、Project 2013、EPM、アーキテクチャ、および Project Server の利点
localization_priority: Normal
ms.assetid: 9ea3b3c1-fb90-454a-b8e6-abc44fca663d
description: このセクションの記事では、Project Professional 2013、Project Server 2013、Project Web App、および SharePoint Server 2013 を組み合わせたエンタープライズ プロジェクト管理 (EPM) ソリューションの全体的なアーキテクチャについて説明します。
ms.openlocfilehash: 44cd5a32b8d3de421ffe3b2d9bf0137146bc4c4e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413788"
---
# <a name="project-server-2013-architecture-and-programmability"></a>Project Server 2013 のアーキテクチャおよびプログラミング

このセクションの記事では、Project Professional 2013、Project Server 2013、Project Web App、および SharePoint Server 2013 を組み合わせたエンタープライズ プロジェクト管理 (EPM) ソリューションの全体的なアーキテクチャについて説明します。
  
Project Server 2013は、.NET Framework 4 で構築され、真のマルチティア アーキテクチャを提供する Project Server の 3 番目のメジャー リリースです。 クラウド アクセスの場合、Project Server 2013 は、Web アプリケーション、モバイル アプリケーション、および Silverlight アプリケーションで使用できるレポート用のクライアント側オブジェクト モデル (CSOM) と OData サービスを実装します。 社内設置型アプリケーションの場合、クライアントは CSOM または Project Server Interface (PSI) サービスを使用できます。 
  
## <a name="introduction-to-project-server-architecture"></a>Project Server アーキテクチャの概要

このセクションのトピックでは、Project Professional 2013、Project Server 2013、Project Web App、および SharePoint Server 2013 を組み合わせたエンタープライズ プロジェクト管理 (EPM) ソリューションの全体的なアーキテクチャについて説明します。
  
Project Server にプログラムでアクセスするには、CSOM または PSI サービスを Windows Communication Foundation (WCF) インターフェイスで使用する必要があります。 PSI の ASMX Web サービス インターフェイスは、Project Server 2013で使用されていませんが、引き続き機能します。 PSI はデータセットの使用による効率的なアクセスを可能にし、サーバー側イベントのハンドラーを作成できます。 CSOM 自身は PSI を使用して、Project Server のビジネス オブジェクト層にアクセスします。 4 つの Project Server データベースの代わりに、Project Server 2013アクセス層で 1 つのデータベースを使用します。
  
Project Server 2013 SharePoint Server 2013 と深く統合されます。 Project アプリケーション サービスは、ファーム内の他の SharePoint サイト コレクションに関連付けることができます。 Project Server はサイト コレクション内の SharePoint タスク リストを操作し、レポートを生成できるほか、Project Server がタスク リストをエンタープライズ プロジェクトとしてインポートおよび管理する場合に完全に制御することもできます。 Project Server では、Windows Workflow Foundation (WF4) のバージョン 4 も使用し、需要管理ソリューションのワークフロー アクティビティを追加します。
  
Project 2013 が開発者に提供する多くの新機能、および非推奨の機能の詳細については、「Project 2013 の開発者向け [更新プログラム」を参照してください](updates-for-developers-in-project-2013.md)。
  
## <a name="in-this-section"></a>このセクションの内容

[Project Server 2013アーキテクチャでは](project-server-2013-architecture.md) 、クライアントやサーバーなど、Project 2013プラットフォームの主要な部分について説明します。 
  
[Project Server のプログラミングでは](project-server-programmability.md) 、Project Server 2013 の主な機能拡張機能、Project Web App のカスタマイズ、以前の Project Server バージョン用に構築されたアプリケーションのアップグレードについて説明します。 
  
「[What the PSI does and does not do](what-the-psi-does-and-does-not-do.md)」では、PSI を使用できるシナリオと PSI で実行できない操作について説明します。 
  
「[What the CSOM does and does not do](what-the-csom-does-and-does-not-do.md)」では、CSOM を使用できるシナリオと CSOM で実行できない操作について説明します。 
  
### <a name="topics-not-covered"></a>扱わない内容

「アーキテクチャとプログラミング」  *セクション*  の記事では、Project デスクトップ クライアント (Project Standard 2013 および Project Professional 2013) またはプロジェクト の機能はProject Web App。 
  
Project Standard および Project Professional 内では、Visual Basic Editor で Visual Basic for Applications (VBA) ヘルプを使用できます。
  
## <a name="see-also"></a>関連項目
<a name="bk_addresources"> </a>

- [Project 2013 における開発者向けの更新内容](updates-for-developers-in-project-2013.md)
    
- [Project Server ワークフロー開発の作業開始](getting-started-developing-project-server-workflows.md)
    

