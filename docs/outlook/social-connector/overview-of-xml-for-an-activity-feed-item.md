---
title: アクティビティ フィード アイテムのための XML の概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 366550fa-e787-4ca0-bfe1-a7890dfc27c6
description: アクティビティ フィードは、ソーシャル ネットワーク上で発生する 1 つ以上のアクティビティで構成されます。 各アクティビティ フィードは activityFeed 要素で表され、次の 3 つの情報が特徴です。
ms.openlocfilehash: 528a7e2c32c7a5c4c2947bfad864accd92fcc419
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566116"
---
# <a name="overview-of-xml-for-an-activity-feed-item"></a>アクティビティ フィード アイテムのための XML の概要

アクティビティ フィードは、ソーシャル ネットワーク上で発生する 1 つ以上のアクティビティで構成されます。 各アクティビティ フィードは **activityFeed** 要素で表され、次の 3 つの情報が特徴です。 
  
- **network**—アクティビティの発信元のソーシャル ネットワークの名前。
    
- **activities**—そのソーシャル ネットワーク上のログオンしているユーザーのアカウントで発生するアクティビティのコンテナー。
    
- **templates**—アクティビティに対応するアクティビティ アイテムを表示するために使用されるテンプレートの **コンテナー** です。
    
アクティビティ フィード アイテムを作成するには、ソーシャル コネクタ (OSC) プロバイダー Outlook XML スキーマに準拠する必要があります。 図 1 は、アクティビティ フィードの XML 構造を示しています。
  
**図 1.アクティビティ フィードの XML 構造**

![アクティビティ XML の構造](media/odc_ol14_ta_OSC_Fig06.gif)
  
各アクティビティ フィード アイテムについて、このスキーマの最も重要な 2 つの部分は **、activityDetails** 要素と **activityTemplateContainer** 要素です。 
  
- **activityDetails** 要素には、アクティビティの所有者の名前やアップロードされた画像の URL など、各アクティビティ フィード アイテムの特定の情報が格納されます。 
    
- **activityTemplateContainer 要素** は、各アクティビティ フィード アイテムの形式またはレイアウトを格納します。 個々の **activityTemplate** 要素で表されるテンプレートで構成され、複数のフィード アイテムに再利用できます。 
    
個々のアクティビティ フィード アイテムの **activityTemplate** 要素は、次の 4 つの情報を指定します。 
  
- **icon**—アクティビティ フィード アイテムを表示するアイコンの URL を指定します。
    
- **title**—アクティビティ フィード アイテムについて説明します。
    
- **type**—状態、写真、ドキュメントの更新など、アクティビティの種類を指定します。
    
- **data**—アクティビティ フィード アイテムと一緒に表示される追加の情報を指定します。
    
> [!TIP]
> アクティビティ フィードに表示されるアイコンは **、ISocialProvider::SocialNetworkIcon** プロパティによって返されるプロバイダー アイコンと常に同じです。 
  
**activityDetails** 要素 **、activityTemplateContainer** 要素、テンプレート トークン、テンプレート変数の詳細については、次のトピックを参照してください。 
  
- [activityDetails 要素](activitydetails-element.md)
    
- [activityTemplateContainer 要素](activitytemplatecontainer-element.md)
    
- [テンプレート変数](template-variables.md)
    
- [アクティビティを適切に表示するためのガイドライン](guidelines-for-properly-displaying-activities.md)
    
アクティビティ フィード XML の例については、「アクティビティ フィード [XML の例」を参照してください](activity-feed-xml-example.md)。
  
## <a name="see-also"></a>関連項目

- [アクティビティの XML](xml-for-activities.md) 
- [Outlookソーシャル コネクタ プロバイダー XML スキーマ](outlook-social-connector-provider-xml-schema.md)
- [OSC XML スキーマを使用したプロバイダーの開発](developing-a-provider-with-the-osc-xml-schema.md)

