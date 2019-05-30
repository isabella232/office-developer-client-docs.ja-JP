---
title: OSC XML スキーマによるプロバイダーの開発
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0872b1b9-c21f-4bba-8cf1-4b010d8d7fb6
description: Outlook Social Connector (.OSC) プロバイダーの XML スキーマは、ソーシャルネットワークから、ネットワークの .OSC プロバイダーを経由して、.OSC に渡される大量の情報の形式を定義します。
ms.openlocfilehash: 2346e23beb2de1664ec90263a8f5db5d46c54e6f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539256"
---
# <a name="developing-a-provider-with-the-osc-xml-schema"></a>OSC XML スキーマによるプロバイダーの開発

Outlook Social Connector (.OSC) プロバイダーの XML スキーマは、ソーシャルネットワークから、ネットワークの .OSC プロバイダーを経由して、.OSC に渡される大量の情報の形式を定義します。 XML スキーマを使用すると、.OSC プロバイダーは、3つの主要な要素、**機能**、**フレンド**、および**activityfeed**、およびその子を使用して、ソーシャルネットワーク上のプロバイダー、フレンド、アクティビティフィードアイテムの機能を指定できます。elements. .OSC プロバイダーは、.osc プロバイダーの拡張機能にインターフェイスとそのメソッドを実装し、XML 文字列を、.OSC プロバイダーの XML スキーマに準拠する出力パラメーターとして返します。 .OSC は、これらのメソッドを呼び出して、XML スキーマで定義されているように理解できる情報を取得します。
  
> [!NOTE]
> .OSC プロバイダー拡張機能は`DebugProviders` `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` 、レジストリキーの値を1に設定することによって、デバッグプロバイダーをサポートします。 プロバイダーデバッグを有効にすると、.OSC は、 **xmlns** xml 属性で指定したバージョンの .osc xml スキーマに対して、プロバイダ xml を検証します。 Outlook Social Connector 2013 以降の .osc 1.1 およびバージョンの .OSC については、次のように**xmlns**属性を指定します。`xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`
  
## <a name="in-this-section"></a>このセクションの内容

- [友人とアクティビティを同期](synchronizing-friends-and-activities.md)する: 各プロバイダーが友人、友人以外、およびソーシャルネットワーク上のアクティビティを同期できるようにするさまざまな方法について説明します。 
    
- [.Osc プロバイダ xml の例](osc-provider-xml-examples.md): .osc xml スキーマを使用して、ソーシャルネットワーク上の .osc プロバイダー、フレンド、アクティビティフィードアイテムの機能を指定する方法を示す XML の例が含まれています。
    
- [機能の xml](xml-for-capabilities.md): この例で[](isocialprovider-getcapabilities.md)は、.osc が機能情報を取得するために、.osc プロバイダーから機能情報を取得する**** ために、.osc で使用されています。 このセクションでは、.osc プロバイダーの XML スキーマの XML 要素についても説明します。これにより、.OSC プロバイダーは、ユーザーの認証方法やフレンドとアクティビティの同期方法などの機能を指定できます。 
    
- [Friends の XML](xml-for-friends.md): friends が、 **friends** XML で表現される友人の情報を、.osc プロバイダーから取得するために、.Osc が使用する api の例を示します。 このセクションでは、 **friends** XML の要素についても説明します。 
    
- [アクティビティ用の XML](xml-for-activities.md): アクティビティ情報を取得するために、.osc がアクティビティ情報を取得する**** ために使用する api の例を、.osc プロバイダーから提供します。 このセクションでは、.OSC プロバイダーがアクティビティフィードを指定できるようにする、.OSC プロバイダーの XML スキーマの XML 要素についても説明します。 アクティビティフィードには、アクティビティフィードのアイテムが送信されたネットワーク、各アクティビティフィードアイテムの詳細 (所有者、種類、アクティビティの発行日など)、およびアクティビティを表示するためのテンプレートが含まれています。 
    
## <a name="reference"></a>リファレンス

- [Outlook Social Connector プロバイダーリファレンス](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>関連情報

- [Outlook Social Connector プロバイダーの開発の概要 (英語)(機械翻訳)](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [.OSC サンプルテンプレート](osc-sample-templates.md)
  
- [通常の呼び出しシーケンスの .OSC](osc-typical-calling-sequences.md)
  
- [プロバイダーをデバッグする](debugging-a-provider.md)
  
- [プロバイダーを展開する](deploying-a-provider.md)
  
- [プロバイダーを開発するためのベストプラクティス](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a>関連項目

- [プロバイダーをデバッグする](debugging-a-provider.md)

