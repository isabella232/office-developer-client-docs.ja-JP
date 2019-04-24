---
title: OSC の典型的な呼び出しシーケンス
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f61960f7-e018-4d2e-8e32-426ed46d9064
description: このセクションでは、.osc プロバイダーが実装している、.osc プロバイダー拡張インターフェイスのメンバーの一般的な呼び出しシーケンス (.osc) について説明します。
ms.openlocfilehash: f7829b710d6840ccd1fa0f990d6e03b2eb879431
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356267"
---
# <a name="osc-typical-calling-sequences"></a>OSC の典型的な呼び出しシーケンス

このセクションでは、.osc プロバイダーが実装している、.osc プロバイダー拡張インターフェイスのメンバーの一般的な呼び出しシーケンス (.osc) について説明します。 典型的な呼び出しシーケンスは、.osc がこのようなインターフェイスやメソッドを使用する方法とタイミングを示しており、プロバイダー拡張インターフェイスに特定のメンバーを実装する方法をより良く判断できるようにします。 実際の通話シーケンスは、 [iime alprovider:: getcapabilities](isocialprovider-getcapabilities.md)メソッドによって返される機能によって異なる場合があります。 機能の例を次に示します。 
  
- プロバイダーは、ソーシャルネットワークからの友人やアクティビティを取得、キャッシュ、または動的に検索するためにサポートされています。
    
- ユーザーがログオンするために、.osc が表示するユーザーインターフェイス。
    
- .osc が使用する認証の種類 (フォームベース認証など)。
    
## <a name="in-this-section"></a>このセクションの内容

- [基本認証](basic-authentication.md): .osc プロバイダーが基本認証をサポートしている場合、ソーシャルネットワークにログオンしている Office ユーザーをサポートするために、.osc の一般的な呼び出しシーケンスについて説明します。
    
- [フォームベース認証](forms-based-authentication.md): .osc プロバイダーがフォームベース認証をサポートしている場合、ソーシャルネットワークにログオンしている Office ユーザーをサポートするために、.osc の一般的な呼び出しシーケンスについて説明します。
    
- [アクティビティの取得](getting-activities.md): ソーシャルネットワークの関連プロバイダーがアクティビティの同期をサポートしている場合は、.osc の一般的な呼び出しシーケンスを、ソーシャルネットワークから同期するように記述します。
    
- [フレンド情報の取得](getting-friends-information.md): ソーシャルネットワークの機能プロバイダーが連絡先のキャッシュされた同期をサポートしている場合は、アプリケーションから Office ユーザーのフレンドリストをソーシャルネットワークから同期するための、.osc の一般的な呼び出しシーケンスについて説明します。
    
## <a name="reference"></a>リファレンス

- [Outlook Social Connector プロバイダーリファレンス](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>関連情報

- [Outlook Social Connector プロバイダーの開発の概要 (英語)(機械翻訳)](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [.osc サンプルテンプレート](osc-sample-templates.md)
  
- [.osc XML スキーマを使用してプロバイダーを開発する](developing-a-provider-with-the-osc-xml-schema.md)
  
- [プロバイダーをデバッグする](debugging-a-provider.md)
  
- [プロバイダーを展開する](deploying-a-provider.md)
  
- [プロバイダーを開発するためのベストプラクティス](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a>関連項目

- [機能の XML](xml-for-capabilities.md)

