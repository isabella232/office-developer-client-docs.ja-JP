---
title: Outlook ソーシャル コネクタ、プロバイダーの開発の概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1c65d2df-86a3-48d5-9fec-a9040f3b878c
description: Outlook ソーシャル コネクタ (OSC) プロバイダーの参照では、OSC プロバイダーの拡張機能を使用して、OSC プロバイダーを開発する方法について説明します。
ms.openlocfilehash: 19f5ffe8987d0b19017692ddb8f7888be2140033
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804325"
---
# <a name="getting-started-with-developing-an-outlook-social-connector-provider"></a>Outlook ソーシャル コネクタ、プロバイダーの開発の概要

Outlook ソーシャル コネクタ (OSC) プロバイダーの参照では、OSC プロバイダーの拡張機能を使用して、OSC プロバイダーを開発する方法について説明します。 Outlook ソリューションの開発に慣れていない場合は、Api とはお客様のニーズに最も適しているテクノロジを確認する[、API または Outlook ソリューションの開発のためのテクノロジを選択する](http://msdn.microsoft.com/library/8295da20-e567-4d08-b8e4-5c9b4498edd4%28Office.15%29.aspx)を参照してください。 

このセクションでは、OSC は、OSC プロバイダーとプロバイダー、技術要件、ベスト ・ プラクティス、プロバイダーを開発するための開発方法の学習の便利なクイック ステップは、どのように、このリリースの新機能の概要を示します。 
  
## <a name="in-this-section"></a>このセクションの内容

- [プロバイダーの新](what-s-new-for-providers.md): OSC の比較は以前のバージョンと現在のリリースでは機能し、インターフェイスのメンバーと追加、変更、またはこのリリースで廃止されている XML スキーマ要素について説明します。 
    
- [Outlook ソーシャル コネクタ プロバイダーを開発する理由](why-develop-an-outlook-social-connector-provider.md): OSC プロバイダーを一般的なソーシャル ネットワーク サイトおよびその他の内部ネットワークのツールは役に立つ方法について説明します。
    
- [関連する Outlook とソーシャル ネットワークと OSC](relating-the-osc-with-outlook-and-social-networks.md): OSC の Outlook ユーザーのソーシャル ネットワークに接続する方法の構造的なビューを提供します。 方法を定義する一般的な用語、「ソーシャル ネットワーク」のように [フレンド]、[フレンド以外、] および [連絡先] は、この参照の残りの部分で使用されます。
    
- [プロバイダーを開発する学習のためのクイック ステップ](quick-steps-for-learning-to-develop-a-provider.md): OSC プロバイダーを開発する方法を説明する手順の概要を提供します。
    
- [技術要件](technical-requirements.md): サポートされているプログラミング言語、COM の可視性の要件、メソッドの戻り値の型の要件、および OSC プロバイダーの拡張機能 DLL の詳細について説明します。
    
- [プロバイダーを開発するためのベスト ・ プラクティス](best-practices-for-developing-a-provider.md): OSC プロバイダーを開発する際に、次のベスト プラクティスの一覧を提供します。
    
## <a name="reference"></a>リファレンス

- [Outlook ソーシャル コネクタ プロバイダーの参照](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>関連セクション

- [OSC サンプル テンプレート](osc-sample-templates.md)
  
- [OSC の典型的な呼び出しシーケンス](osc-typical-calling-sequences.md)
  
- [OSC の XML スキーマを使用してプロバイダーの開発](developing-a-provider-with-the-osc-xml-schema.md)
  
- [プロバイダーのデバッグ](debugging-a-provider.md)
  
- [プロバイダーを展開します。](deploying-a-provider.md)
  
- [OSC プロバイダーをリリースする準備をします。](getting-ready-to-release-an-osc-provider.md)
  
## <a name="see-also"></a>関連項目

- [Microsoft Outlook ソーシャル コネクタ 32 ビット](http://www.microsoft.com/downloads/details.aspx?FamilyID=b638cc14-11e5-448a-b5a6-4f553ce81b94)
- [Outlook ソーシャル コネクタ (KB983403)、32 ビット版用の更新プログラム](http://www.microsoft.com/downloads/details.aspx?FamilyID=9886faca-f1c5-4579-83e2-c872c7abc61a)
- [Outlook ソーシャル コネクタ (KB983403)、64 ビット版用の更新プログラム](http://www.microsoft.com/downloads/details.aspx?FamilyID=72a506a7-8a91-4d56-8b27-bf3b3f58fe9a)
- [Outlook ソーシャル コネクタ 2013: プロバイダー テンプレート](http://code.msdn.microsoft.com/Outlook-Social-Connector-73fd8d2c)

