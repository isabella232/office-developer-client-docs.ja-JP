---
title: OSC の典型的な呼び出しシーケンス
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f61960f7-e018-4d2e-8e32-426ed46d9064
description: OSC プロバイダーの機能拡張インターフェイス、OSC プロバイダーを実装しているメンバーの Outlook ソーシャル コネクタ (OSC) 典型的な呼び出しのシーケンスを説明します。
ms.openlocfilehash: 4a79e27fadb78933f41f26818cfab8b7f4a5aae7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804451"
---
# <a name="osc-typical-calling-sequences"></a>OSC の典型的な呼び出しシーケンス

OSC プロバイダーの機能拡張インターフェイス、OSC プロバイダーを実装しているメンバーの Outlook ソーシャル コネクタ (OSC) 典型的な呼び出しのシーケンスを説明します。 典型的な呼び出しシーケンスは、時期と方法を示して、OSC は、このようなインターフェイスを使用し、向上できるように、メソッドがプロバイダーの機能拡張インターフェイスで特定のメンバーを実装する方法を決定します。 実際の呼び出しのシーケンスは、 [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)メソッドによって返される機能によって異なります。 機能の例を以下に示します。 
  
- プロバイダーを取得する、キャッシュ、または動的に友人や活動を検索、ソーシャル ネットワークからのサポートします。
    
- ユーザー インターフェイスは、ユーザー ログオン用の OSC を表示する必要があります。
    
- 認証の種類 (たとえば、フォーム ベース認証の場合)、OSC を使用する必要があります。
    
## <a name="in-this-section"></a>このセクションの内容

- [基本認証](basic-authentication.md): OSC プロバイダーは、基本認証をサポートしている場合は、ソーシャル ネットワークにログオンしている Office ユーザーをサポートするために OSC の典型的な呼び出しシーケンスを説明します。
    
- [フォーム ベースの認証](forms-based-authentication.md): OSC プロバイダーは、フォーム ベース認証をサポートしている場合は、ソーシャル ネットワークにログオンしている Office ユーザーをサポートするために OSC の典型的な呼び出しシーケンスを説明します。
    
- [活動を取得する](getting-activities.md): ソーシャル ネットワーク OSC プロバイダーは、アクティビティの同期をサポートしている場合は、ソーシャル ネットワーク経由で Office ユーザーの友人の動作を同期するのには OSC の典型的な呼び出しシーケンスを説明します。
    
- [フレンド情報の取得](getting-friends-information.md): ソーシャル ネットワーク OSC プロバイダーが連絡先のキャッシュの同期をサポートしている場合は、ソーシャル ネットワーク経由での Office ユーザーのフレンド リストを同期するのには OSC の典型的な呼び出しシーケンスを説明します。
    
## <a name="reference"></a>リファレンス

- [Outlook ソーシャル コネクタ プロバイダーの参照](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>関連セクション

- [Outlook Social Connector プロバイダーの開発の概要 (英語)(機械翻訳)](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [OSC サンプル テンプレート](osc-sample-templates.md)
  
- [OSC の XML スキーマを使用してプロバイダーの開発](developing-a-provider-with-the-osc-xml-schema.md)
  
- [プロバイダーのデバッグ](debugging-a-provider.md)
  
- [プロバイダーを展開します。](deploying-a-provider.md)
  
- [プロバイダーを開発するためのベスト プラクティス](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a>関連項目

- [機能のための XML](xml-for-capabilities.md)

