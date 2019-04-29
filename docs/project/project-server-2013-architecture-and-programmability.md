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
- プロジェクト2013、アーキテクチャとプログラミング、プログラミング、project Server、project 2013、EPM、アーキテクチャ、および Project Server の利点
localization_priority: Normal
ms.assetid: 9ea3b3c1-fb90-454a-b8e6-abc44fca663d
description: このセクションの記事では、project Professional 2013、project Server 2013、project Web App、および SharePoint Server 2013 を組み合わせた epm (Enterprise project Management) ソリューションの全体的なアーキテクチャについて説明します。
ms.openlocfilehash: 44cd5a32b8d3de421ffe3b2d9bf0137146bc4c4e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413788"
---
# <a name="project-server-2013-architecture-and-programmability"></a>Project Server 2013 のアーキテクチャおよびプログラミング

このセクションの記事では、project Professional 2013、project Server 2013、project Web App、および SharePoint Server 2013 を組み合わせた epm (Enterprise project Management) ソリューションの全体的なアーキテクチャについて説明します。
  
project server 2013 は .net Framework 4 を使用して構築されています。これは、project server の第3メジャーリリースで、真の多層アーキテクチャを提供します。 クラウドアクセスの場合、Project Server 2013 は、クライアント側オブジェクトモデル (csom) と、web アプリケーション、モバイルアプリケーション、および Silverlight アプリケーションで使用できるレポート用の OData サービスを実装します。 社内設置型アプリケーションの場合、クライアントは CSOM または Project Server Interface (PSI) サービスを使用できます。 
  
## <a name="introduction-to-project-server-architecture"></a>Project Server アーキテクチャの概要

このセクションのトピックでは、project Professional 2013、project Server 2013、project Web App、および SharePoint Server 2013 を組み合わせた epm (Enterprise project Management) ソリューションの全体的なアーキテクチャについて説明します。
  
Project Server にプログラムでアクセスするには、Windows Communication Foundation (WCF) インターフェイスで csom または PSI サービスのいずれかを使用する必要があります。 PSI の ASMX web サービスインターフェイスは、Project Server 2013 で廃止されましたが、まだ機能します。 PSI はデータセットの使用による効率的なアクセスを可能にし、サーバー側イベントのハンドラーを作成できます。 CSOM 自身は PSI を使用して、Project Server のビジネス オブジェクト層にアクセスします。 project server 2013 は、4つの project server データベースではなく、1つのデータベースをデータアクセス層に使用します。
  
Project server 2013 は、SharePoint server 2013 と緊密に統合されています。 Project アプリケーション サービスは、ファーム内の他の SharePoint サイト コレクションに関連付けることができます。 Project Server はサイト コレクション内の SharePoint タスク リストを操作し、レポートを生成できるほか、Project Server がタスク リストをエンタープライズ プロジェクトとしてインポートおよび管理する場合に完全に制御することもできます。 また、Project Server は、Windows Workflow Foundation (WF4) のバージョン4を使用し、需要管理ソリューションのワークフローアクティビティを追加します。
  
開発者に対して Project 2013 が提供する多くの新機能と廃止される機能の説明については、「 [project 2013 の開発者向けの更新プログラム](updates-for-developers-in-project-2013.md)」を参照してください。
  
## <a name="in-this-section"></a>このセクションの内容

[project Server 2013 アーキテクチャ](project-server-2013-architecture.md)クライアントおよびサーバーを含む、project 2013 プラットフォームの主要な部分について説明します。 
  
[project server プログラミング](project-server-programmability.md)では、project server 2013 の主な拡張機能、project Web App のカスタマイズ、および以前の project server バージョン用に構築されたアプリケーションのアップグレードについて説明しています。 
  
「[What the PSI does and does not do](what-the-psi-does-and-does-not-do.md)」では、PSI を使用できるシナリオと PSI で実行できない操作について説明します。 
  
「[What the CSOM does and does not do](what-the-csom-does-and-does-not-do.md)」では、CSOM を使用できるシナリオと CSOM で実行できない操作について説明します。 
  
### <a name="topics-not-covered"></a>扱わない内容

「*アーキテクチャおよびプログラミング*」セクションの記事では、プロジェクトデスクトップクライアント (project Standard 2013 および project Professional 2013) または project Web App の機能については文書化されていません。 
  
Project Standard および Project Professional 内では、Visual Basic Editor で Visual Basic for Applications (VBA) ヘルプを使用できます。
  
## <a name="see-also"></a>関連項目
<a name="bk_addresources"> </a>

- [Project 2013 における開発者向けの更新内容](updates-for-developers-in-project-2013.md)
    
- [Project Server ワークフロー開発の作業開始](getting-started-developing-project-server-workflows.md)
    

