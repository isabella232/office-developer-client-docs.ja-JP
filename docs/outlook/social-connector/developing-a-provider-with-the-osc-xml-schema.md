---
title: OSC XML スキーマによるプロバイダーの開発
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0872b1b9-c21f-4bba-8cf1-4b010d8d7fb6
description: Outlook ソーシャル コネクタ (OSC) プロバイダーの XML スキーマでは、膨大な OSC をソーシャル ネットワークからネットワークの OSC プロバイダーを通じて渡される情報の形式を定義します。
ms.openlocfilehash: 75809179131ce6c6b8bbe171d2670e59cebe3494
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390549"
---
# <a name="developing-a-provider-with-the-osc-xml-schema"></a>OSC XML スキーマによるプロバイダーの開発

Outlook ソーシャル コネクタ (OSC) プロバイダーの XML スキーマでは、膨大な OSC をソーシャル ネットワークからネットワークの OSC プロバイダーを通じて渡される情報の形式を定義します。 XML スキーマでは、プロバイダー、友人、またはアクティビティ フィードのアイテムの 3 つの主要な要素、**機能**、**友人**、および**activityFeed**、およびその子を使用して、ソーシャル ネットワーク上の機能を指定するのには、OSC プロバイダー要素です。 OSC プロバイダーにより、OSC プロバイダーの機能拡張のインターフェイスとそのメソッドを実装 OSC プロバイダーの XML スキーマに準拠している出力パラメーターとしての XML 文字列を返すことが実現します。 OSC では、XML スキーマで定義されていることが理解できる情報を取得するこれらのメソッドを呼び出します。
  
> [!NOTE]
> OSC プロバイダーの拡張機能を設定してプロバイダーのデバッグをサポートする、`DebugProviders`の値、`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector`レジストリ キーを 1 にします。 プロバイダーのデバッグを有効にすると、OSC は、 **xmlns**の XML 属性で指定した OSC の XML スキーマのバージョンとプロバイダーの XML を検証します。 OSC 1.1 とバージョンの Outlook ソーシャル コネクタ 2013 以降の OSC は、次のように、 **xmlns**属性を指定します。`xmlns="https://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`
  
## <a name="in-this-section"></a>このセクションの内容

- [同期の友人と活動](synchronizing-friends-and-activities.md): OSC プロバイダーが友人、友人以外の場合、およびソーシャル ネットワーク上のアクティビティを同期できること、さまざまな方法について説明します。 
    
- [OSC プロバイダーの XML の例](osc-provider-xml-examples.md): を含む XML の例を示します、OSC プロバイダー、友人、およびアクティビティの機能を指定するのにはソーシャル ネットワークの OSC の XML スキーマを使用してアイテムをフィードします。
    
- [機能のための XML](xml-for-capabilities.md): 説明 - [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) OSC を使用するメソッド**の機能**、XML から OSC プロバイダーで表される機能情報を取得します。 OSC プロバイダーなど、どのようにユーザーを認証して、友人との活動を同期化の機能を指定できるように、OSC プロバイダーの XML スキーマ内の XML 要素についても説明します。 
    
- [友人の XML](xml-for-friends.md): OSC を使用して**友人**、XML OSC プロバイダーからで表される、友人の情報を取得する Api の例を紹介します。 **友人**XML 内の要素についても説明します。 
    
- [アクティビティ用の XML](xml-for-activities.md): OSC を使用してアクティビティについては、 **activityFeed** XML、OSC プロバイダーからの表現を取得する Api の例を紹介します。 OSC プロバイダー、アクティビティ フィードを指定できるように、OSC プロバイダーの XML スキーマ内の XML 要素についても説明します。 アクティビティ フィードには、ネットワーク アクティビティが発生した場合、アイテムをフィードごとのアクティビティ フィードのアイテムの詳細が含まれています (などの所有者は、入力、発行とアクティビティの日付)、および活動を表示するテンプレートです。 
    
## <a name="reference"></a>リファレンス

- [Outlook ソーシャル コネクタ プロバイダーの参照](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>関連情報

- [Outlook Social Connector プロバイダーの開発の概要 (英語)(機械翻訳)](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [OSC サンプル テンプレート](osc-sample-templates.md)
  
- [OSC の典型的な呼び出しシーケンス](osc-typical-calling-sequences.md)
  
- [プロバイダーのデバッグ](debugging-a-provider.md)
  
- [プロバイダーを展開します。](deploying-a-provider.md)
  
- [プロバイダーを開発するためのベスト プラクティス](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a>関連項目

- [プロバイダーのデバッグ](debugging-a-provider.md)

