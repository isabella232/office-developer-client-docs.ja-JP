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
- プロジェクト 2013、EPM、アーキテクチャ、および Project Server のアーキテクチャおよびプログラミング、プログラミング、サーバーのプロジェクト、Project 2013 の利点
localization_priority: Normal
ms.assetid: 9ea3b3c1-fb90-454a-b8e6-abc44fca663d
description: このセクションの記事では、エンタープライズ プロジェクト管理 (EPM) ソリューションでは、評価のためのプロジェクトを Project Server 2013、Project Web App では、SharePoint Server 2013 を組み合わせたものの全体的なアーキテクチャについて説明します。
ms.openlocfilehash: 6b5ab94968dbb996a370e0e5abb89813f5e41ef7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804685"
---
# <a name="project-server-2013-architecture-and-programmability"></a>Project Server 2013 のアーキテクチャおよびプログラミング

このセクションの記事では、エンタープライズ プロジェクト管理 (EPM) ソリューションでは、評価のためのプロジェクトを Project Server 2013、Project Web App では、SharePoint Server 2013 を組み合わせたものの全体的なアーキテクチャについて説明します。
  
Project Server 2013 は、.NET Framework 4 で作成された、真の多階層アーキテクチャを提供するのには Project Server の 3 番目のメジャー リリースです。 クラウドへのアクセスの Project Server 2013 は、web アプリケーション、モバイル アプリケーション、および Silverlight アプリケーションでクライアント側オブジェクト モデル (CSOM) とレポート作成のために使用できる OData サービスを実装します。 設置型のアプリケーションでは、クライアントは、CSOM またはプロジェクト Server インターフェイス (PSI) のサービスのいずれかを使用できます。 
  
## <a name="introduction-to-project-server-architecture"></a>Project Server アーキテクチャの概要

このセクションのトピックでは、エンタープライズ プロジェクト管理 (EPM) ソリューションでは、評価のためのプロジェクトを Project Server 2013、Project Web App では、SharePoint Server 2013 を組み合わせたものの全体的なアーキテクチャについて説明します。
  
Project Server にプログラムによるアクセスは、Windows Communication Foundation (WCF) インターフェイスを使用して、CSOM または PSI サービスのいずれかを使用する必要があります。 PSI の ASMX web サービスのインタ フェースは、Project Server 2013 のでは使用されなくなりましたは引き続き機能します。 PSI は、データセットを使用して、効率的なアクセスを有効にし、サーバー側イベントのハンドラーを作成することができます。 自体 CSOM は、Project Server のビジネス オブジェクト層にアクセスするのには、PSI を使用します。 4 つの Project Server データベースの代わりには、Project Server 2013 は、データ アクセス層で 1 つのデータベースを使用します。
  
Project Server 2013 は、SharePoint Server 2013 で緊密に統合されています。 Project アプリケーション サービスは、ファーム内の他の SharePoint サイト コレクションに関連付けることができます。 Project Server で動作でき、レポートでは、サイト コレクションでは、タスク ・ リストも、Project Server のインポートし、管理、フル コントロールを取得する SharePoint のエンタープライズ プロジェクトのタスク一覧を表示することができます。 Project Server は、Windows ワークフロー Foundation (WF4) のバージョン 4 を使用してもと需要管理ソリューションのワークフロー アクティビティを追加します。
  
開発者は、Project 2013 が提供する多くの新機能と廃止される機能については、 [Project 2013 の開発者用の更新プログラム](updates-for-developers-in-project-2013.md)を参照してください。
  
## <a name="in-this-section"></a>このセクションの内容

[Project Server 2013 のアーキテクチャ](project-server-2013-architecture.md)では、クライアントとサーバーを含む、Project 2013 のプラットフォームの主要な部分について説明します。 
  
[Project Server プログラミング](project-server-programmability.md)では、Project Server 2013、Project Web App では、Project Server の以前のバージョン用に構築されたアプリケーションのアップグレードのカスタマイズの主要な拡張機能について説明します。 
  
「[What the PSI does and does not do](what-the-psi-does-and-does-not-do.md)」では、PSI を使用できるシナリオと PSI で実行できない操作について説明します。 
  
「[What the CSOM does and does not do](what-the-csom-does-and-does-not-do.md)」では、CSOM を使用できるシナリオと CSOM で実行できない操作について説明します。 
  
### <a name="topics-not-covered"></a>扱わない内容

*アーキテクチャおよびプログラミング*のセクションの記事には、デスクトップ クライアントを (プロジェクトの標準的な 2013 および評価のためのプロジェクト) は、プロジェクトまたは Project Web App の機能は文書化されません。 
  
Project Standard および Project Professional 内では、Visual Basic Editor で Visual Basic for Applications (VBA) ヘルプを使用できます。
  
## <a name="see-also"></a>関連項目
<a name="bk_addresources"> </a>

- [Project 2013 の開発者向けの新機能](updates-for-developers-in-project-2013.md)
    
- [Project Server ワークフローの開発を開始する](getting-started-developing-project-server-workflows.md)
    

