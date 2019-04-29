---
title: アクティビティ フィード アイテムのための XML の概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 366550fa-e787-4ca0-bfe1-a7890dfc27c6
description: アクティビティフィードは、ソーシャルネットワーク上で発生する1つ以上のアクティビティで構成されます。 各アクティビティフィードは activityfeed 要素で表され、次の3つの情報によって特徴付けられます。
ms.openlocfilehash: 971c54cf69a65bebbe4fd04e8608e88b89145bb4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439948"
---
# <a name="overview-of-xml-for-an-activity-feed-item"></a>アクティビティ フィード アイテムのための XML の概要

アクティビティフィードは、ソーシャルネットワーク上で発生する1つ以上のアクティビティで構成されます。 各アクティビティフィードは**activityfeed**要素で表され、次の3つの情報によって特徴付けられます。 
  
- **network**—アクティビティが開始されたソーシャルネットワークの名前。
    
- **アクティビティ**—ソーシャルネットワークにログオンしているユーザーのアカウントで行われているアクティビティのコンテナー。
    
- **templates**—**アクティビティ**に対応するアクティビティアイテムを表示するために使用されるテンプレートのコンテナー。
    
アクティビティフィードアイテムを作成するには、Outlook Social Connector (.osc) プロバイダ拡張 XML スキーマに準拠している必要があります。 図1は、アクティビティフィード XML データ構造を示しています。
  
**図1。アクティビティフィード XML データ構造**

![アクティビティ XML の構造](media/odc_ol14_ta_OSC_Fig06.gif)
  
アクティビティフィードアイテムごとに、このスキーマの最も重要な2つの部分は**activitydetails**要素と**activitytemplatecontainer**要素です。 
  
- **activitydetails**要素は、アクティビティ所有者の名前や、アップロードされた画像の URL など、アクティビティフィードアイテムごとに固有の情報を格納します。 
    
- **activitytemplatecontainer**要素は、各アクティビティフィードアイテムの形式またはレイアウトを格納します。 個別の**activitytemplate**要素で表されるテンプレートで構成され、複数のフィードアイテムに再利用できます。 
    
個別のアクティビティフィードアイテムの場合、 **activitytemplate**要素は次の4つの情報を指定します。 
  
- **icon**—アクティビティフィードアイテムを表示するアイコンの URL を指定します。
    
- [**タイトル**]: アクティビティフィードアイテムを記述します。
    
- **種類**—状態、写真、ドキュメントの更新など、アクティビティの種類を指定します。
    
- **データ**—アクティビティフィードアイテムと共に表示されるその他の情報を指定します。
    
> [!TIP]
> アクティビティフィードに表示されるアイコンは、常に、i/////"/"/"/入力された" **networkicon**プロパティによって返されるプロバイダアイコンと同じです。 
  
**activitydetails**要素、 **activitytemplatecontainer**要素、テンプレートトークン、およびテンプレート変数の詳細については、以下のトピックを参照してください。 
  
- [activitydetails 要素](activitydetails-element.md)
    
- [activitytemplatecontainer 要素](activitytemplatecontainer-element.md)
    
- [テンプレート変数](template-variables.md)
    
- [アクティビティを適切に表示するためのガイドライン](guidelines-for-properly-displaying-activities.md)
    
アクティビティフィード xml の例については、「[アクティビティフィード xml の例](activity-feed-xml-example.md)」を参照してください。
  
## <a name="see-also"></a>関連項目

- [アクティビティの XML](xml-for-activities.md) 
- [Outlook Social Connector プロバイダーの XML スキーマ](outlook-social-connector-provider-xml-schema.md)
- [.osc XML スキーマを使用してプロバイダーを開発する](developing-a-provider-with-the-osc-xml-schema.md)

