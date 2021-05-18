---
title: OSC の典型的な呼び出しシーケンス
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f61960f7-e018-4d2e-8e32-426ed46d9064
description: このセクションでは、OSC プロバイダー Outlook実装する OSC プロバイダー拡張インターフェイスのメンバーの Outlook ソーシャル コネクタ (OSC) の一般的な呼び出しシーケンスについて説明します。
ms.openlocfilehash: f7829b710d6840ccd1fa0f990d6e03b2eb879431
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413613"
---
# <a name="osc-typical-calling-sequences"></a>OSC の典型的な呼び出しシーケンス

このセクションでは、OSC プロバイダー Outlook実装する OSC プロバイダー拡張インターフェイスのメンバーの Outlook ソーシャル コネクタ (OSC) の一般的な呼び出しシーケンスについて説明します。 一般的な呼び出しシーケンスは、OSC がこのようなインターフェイスとメソッドを使用する方法と時間を示し、プロバイダー拡張インターフェイスに特定のメンバーを実装する方法をより適切に決定できます。 実際の呼び出しシーケンスは [、ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) メソッドによって返される機能によって異なります。 機能の例を次に示します。 
  
- ソーシャル ネットワークからフレンドやアクティビティを取得、キャッシュ、または動的に参照するプロバイダーのサポート。
    
- ユーザー ログオンのために OSC が表示するユーザー インターフェイス。
    
- OSC で使用する認証の種類 (フォーム ベース認証など)。
    
## <a name="in-this-section"></a>このセクションの内容

- [基本認証](basic-authentication.md): OSC プロバイダーが基本認証をサポートしている場合に、ソーシャル ネットワークにログオンしている Office ユーザーをサポートする OSC の一般的な呼び出しシーケンスについて説明します。
    
- [フォーム ベース認証](forms-based-authentication.md): OSC プロバイダーがフォーム ベース認証をサポートしている場合に、ソーシャル ネットワークにログオンしている Office ユーザーをサポートする OSC の一般的な呼び出しシーケンスについて説明します。
    
- [Getting Activities](getting-activities.md): ソーシャル ネットワーク OSC プロバイダーがアクティビティの同期をサポートしている場合に、Office ユーザーのフレンドのアクティビティをソーシャル ネットワークから同期する OSC の一般的な呼び出しシーケンスについて説明します。
    
- [フレンド情報の](getting-friends-information.md)取得 : ソーシャル ネットワーク OSC プロバイダーが連絡先のキャッシュ同期をサポートしている場合に、ソーシャル ネットワークから Office ユーザーのフレンド リストを同期する OSC の一般的な呼び出しシーケンスについて説明します。
    
## <a name="reference"></a>参照

- [Outlookソーシャル コネクタ プロバイダーリファレンス](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>関連情報

- [Outlook Social Connector プロバイダーの開発の概要 (英語)(機械翻訳)](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [OSC サンプル テンプレート](osc-sample-templates.md)
  
- [OSC XML スキーマを使用したプロバイダーの開発](developing-a-provider-with-the-osc-xml-schema.md)
  
- [プロバイダーのデバッグ](debugging-a-provider.md)
  
- [プロバイダーの展開](deploying-a-provider.md)
  
- [プロバイダーの開発に関するベスト プラクティス](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a>関連項目

- [機能の XML](xml-for-capabilities.md)

