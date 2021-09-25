---
title: OSC XML スキーマによるプロバイダーの開発
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 0872b1b9-c21f-4bba-8cf1-4b010d8d7fb6
description: Outlook ソーシャル コネクタ (OSC) プロバイダー XML スキーマは、ネットワークの OSC プロバイダーを介してソーシャル ネットワークから OSC に渡される大量の情報の形式を定義します。
ms.openlocfilehash: 45a9fcc2aab435b4b82e42b80e6601ca2ef2f7f1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629180"
---
# <a name="developing-a-provider-with-the-osc-xml-schema"></a>OSC XML スキーマによるプロバイダーの開発

Outlook ソーシャル コネクタ (OSC) プロバイダー XML スキーマは、ネットワークの OSC プロバイダーを介してソーシャル ネットワークから OSC に渡される大量の情報の形式を定義します。 XML スキーマを使用すると、OSC プロバイダーは、3 つの主要な要素、機能、フレンド、activityFeed、および子要素を使用して、ソーシャルネットワーク上のプロバイダー、フレンド、アクティビティ フィード アイテムの機能を指定できます。 OSC プロバイダーは、OSC プロバイダーの機能拡張にインターフェイスとそのメソッドを実装し、OSC プロバイダー XML スキーマに準拠する出力パラメーターとして XML 文字列を返します。 OSC は、これらのメソッドを呼び出して、XML スキーマで定義されている情報を取得します。
  
> [!NOTE]
> OSC プロバイダーの機能拡張は、レジストリ キーの値を 1 に設定することで、デバッグ プロバイダー `DebugProviders`  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` をサポートします。 プロバイダーのデバッグを有効にした場合、OSC は **xmlns** XML 属性で指定した OSC XML スキーマのバージョンに対してプロバイダー XML を検証します。 ソーシャル コネクタ 2013 以降の OSC 1.1 およびバージョンOutlook **xmlns** 属性を次のように指定します。`xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`
  
## <a name="in-this-section"></a>このセクションの内容

- [フレンドとアクティビティの同期](synchronizing-friends-and-activities.md): OSC プロバイダーがフレンド、フレンド以外、ソーシャル ネットワーク上のアクティビティを同期できるさまざまな方法について説明します。 
    
- [OSC プロバイダー XML](osc-provider-xml-examples.md)の例 : OSC XML スキーマを使用して、ソーシャル ネットワーク上の OSC プロバイダー、フレンド、およびアクティビティ フィード アイテムの機能を指定する方法を示す XML 例が含まれています。
    
- [機能の XML](xml-for-capabilities.md): OSC が OSC プロバイダーから機能 **XML** で表される機能情報を取得するために使用する - [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)メソッドについて説明します。 このセクションでは、OSC プロバイダーがユーザーを認証し、友人やアクティビティを同期する方法など、OSC プロバイダーが機能を指定できる OSC プロバイダー XML スキーマの XML 要素について説明します。 
    
- [[フレンド用 XML]:](xml-for-friends.md)OSC がフレンド **XML** で表されるフレンドの情報を OSC プロバイダーから取得するために使用する API の例を示します。 このセクションでは、フレンド XML の要素について **説明** します。 
    
- [アクティビティの XML](xml-for-activities.md): OSC プロバイダーから **activityFeed** XML で表されるアクティビティ情報を取得するために OSC が使用する API の例を示します。 このセクションでは、OSC プロバイダーがアクティビティ フィードを指定できる OSC プロバイダー XML スキーマの XML 要素について説明します。 アクティビティ フィードには、アクティビティ フィード アイテムが発生したネットワーク、各アクティビティ フィード アイテムの詳細 (アクティビティの所有者、種類、発行日など)、アクティビティを表示するテンプレートが含まれます。 
    
## <a name="reference"></a>リファレンス

- [Outlookソーシャル コネクタ プロバイダーリファレンス](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>関連情報

- [Outlook Social Connector プロバイダーの開発の概要 (英語)(機械翻訳)](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [OSC サンプル テンプレート](osc-sample-templates.md)
  
- [OSC の一般的な呼び出しシーケンス](osc-typical-calling-sequences.md)
  
- [プロバイダーのデバッグ](debugging-a-provider.md)
  
- [プロバイダーの展開](deploying-a-provider.md)
  
- [プロバイダーの開発に関するベスト プラクティス](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a>関連項目

- [プロバイダーのデバッグ](debugging-a-provider.md)

