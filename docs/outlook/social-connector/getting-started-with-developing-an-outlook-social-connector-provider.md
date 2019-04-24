---
title: Outlook Social Connector プロバイダーの開発の概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1c65d2df-86a3-48d5-9fec-a9040f3b878c
description: Outlook Social Connector (.osc) プロバイダリファレンスは、.osc プロバイダー拡張機能を使用して、.osc プロバイダーを開発する方法について説明します。
ms.openlocfilehash: 24f8eabe33103f53e848f055b72fd402bc5dd89a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327161"
---
# <a name="getting-started-with-developing-an-outlook-social-connector-provider"></a>Outlook Social Connector プロバイダーの開発の概要

Outlook Social Connector (.osc) プロバイダリファレンスは、.osc プロバイダー拡張機能を使用して、.osc プロバイダーを開発する方法について説明します。 Outlook のソリューション開発に慣れていない場合、「[Selecting an API or Technology for Developing Outlook Solutions](https://msdn.microsoft.com/library/8295da20-e567-4d08-b8e4-5c9b4498edd4%28Office.15%29.aspx)」をご覧になり、ご自身の必要に最も適した API とテクノロジを識別してください。 

このセクションでは、.osc の概要、.osc プロバイダーが役に立つ方法、プロバイダーの開発方法、技術要件、プロバイダーを開発するためのベストプラクティス、およびこのリリースの新機能について説明します。 
  
## <a name="in-this-section"></a>このセクションの内容

- [プロバイダーの新](what-s-new-for-providers.md)機能: 以前のリリースと現在のリリースの .osc 機能を比較し、このリリースで追加、変更、または廃止されたインターフェイスメンバーと XML スキーマ要素について説明します。 
    
- [Outlook Social Connector プロバイダーを開発する理由](why-develop-an-outlook-social-connector-provider.md): .osc プロバイダーが、一般的なソーシャルネットワークサイトやその他の内部ネットワークツールでどのように役立つかについて説明します。
    
- [.osc と outlook およびソーシャルネットワークと](relating-the-osc-with-outlook-and-social-networks.md)の関係: この例では、.osc が outlook ユーザーとソーシャルネットワークを接続する方法についてのアーキテクチャビューを示します。 また、このリファレンスの残りの部分では、「ソーシャルネットワーク」、「友人」、「友人以外」、「連絡先」などの一般的な用語を使用する方法も定義します。
    
- [プロバイダーを開発するための簡単な手順](quick-steps-for-learning-to-develop-a-provider.md): タスクの概要について説明します。この概要では、.osc プロバイダーを開発する方法について説明します。
    
- [技術要件](technical-requirements.md): サポートされているプログラミング言語、COM の可視性の要件、メソッドの戻り値の型の要件、および .osc プロバイダ拡張 DLL の詳細について説明します。
    
- [プロバイダーを開発するためのベストプラクティス](best-practices-for-developing-a-provider.md): .osc プロバイダーの開発時に従うベストプラクティスの一覧を示します。
    
## <a name="reference"></a>リファレンス

- [Outlook Social Connector プロバイダーリファレンス](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>関連情報

- [.osc サンプルテンプレート](osc-sample-templates.md)
  
- [通常の呼び出しシーケンスの .osc](osc-typical-calling-sequences.md)
  
- [.osc XML スキーマを使用してプロバイダーを開発する](developing-a-provider-with-the-osc-xml-schema.md)
  
- [プロバイダーをデバッグする](debugging-a-provider.md)
  
- [プロバイダーを展開する](deploying-a-provider.md)
  
- [.osc プロバイダーをリリースする準備をする](getting-ready-to-release-an-osc-provider.md)
  
## <a name="see-also"></a>関連項目

- [Microsoft Outlook Social Connector 32 ビット](https://www.microsoft.com/downloads/details.aspx?FamilyID=b638cc14-11e5-448a-b5a6-4f553ce81b94)
- [Outlook Social Connector (KB983403)、32ビット版の更新プログラム](https://www.microsoft.com/downloads/details.aspx?FamilyID=9886faca-f1c5-4579-83e2-c872c7abc61a)
- [Outlook Social Connector (KB983403)、64ビット版の更新プログラム](https://www.microsoft.com/downloads/details.aspx?FamilyID=72a506a7-8a91-4d56-8b27-bf3b3f58fe9a)
- [Outlook Social Connector 2013: プロバイダーテンプレート](https://code.msdn.microsoft.com/Outlook-Social-Connector-73fd8d2c)

