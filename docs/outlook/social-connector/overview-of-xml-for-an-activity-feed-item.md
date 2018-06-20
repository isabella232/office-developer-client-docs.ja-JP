---
title: フィード項目のアクティビティの XML の概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 366550fa-e787-4ca0-bfe1-a7890dfc27c6
description: アクティビティ フィードは、ソーシャル ネットワーク上で発生する 1 つまたは複数のアクティビティで構成されています。 各アクティビティ フィードは、activityFeed 要素によって表されるし、の特徴は、これら 3 つの情報。
ms.openlocfilehash: 318875aeb6312a3710654d129f3f48139ff7ef12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804472"
---
# <a name="overview-of-xml-for-an-activity-feed-item"></a>フィード項目のアクティビティの XML の概要

アクティビティ フィードは、ソーシャル ネットワーク上で発生する 1 つまたは複数のアクティビティで構成されています。 各アクティビティ フィードは、 **activityFeed**要素によって表されるし、の特徴は、これら 3 つの情報。 
  
- **ネットワーク**-活動の起点となるソーシャル ネットワークの名前です。
    
- **活動**ソーシャル ネットワークにログオンしたユーザーのアカウントで発生するアクティビティのコンテナーです。
    
- **テンプレート**など**の活動**に対応する活動項目を表示するために使用するテンプレートのコンテナーです。
    
アクティビティ フィードのアイテムを作成するには、Outlook ソーシャル コネクタ (OSC) プロバイダーの拡張機能の XML スキーマに準拠する必要があります。 アクティビティ フィードの XML の構造を図 1 に示します。
  
**図 1 です。アクティビティ フィードの XML データ構造**

![アクティビティ XML の構造](media/odc_ol14_ta_OSC_Fig06.gif)
  
各アクティビティでは、フィードのアイテム、このスキーマの 2 つの最も重要な部分は、 **activityDetails**と**activityTemplateContainer**の要素。 
  
- **ActivityDetails**要素は、各アクティビティは、アクティビティの所有者の名前またはアップロードする画像の URL などのアイテムのフィードに固有の情報を格納します。 
    
- **ActivityTemplateContainer**要素の形式を格納する、またはフィード項目の各アクティビティのレイアウトです。 テンプレート、複数のフィード項目を再利用できる個々 の**activityTemplate**の要素で表されるので構成されます。 
    
個々 のアクティビティ フィードのアイテムには、 **activityTemplate**要素は、次の 4 つの情報を指定します。 
  
- **アイコン**-フィード項目のアクティビティを表示するアイコンの URL を指定します。
    
- **タイトル**: アクティビティ フィードの項目を説明します。
    
- **タイプ**ステータス、写真、またはドキュメントの更新など、活動の種類を指定します。
    
- **データ**: アクティビティ フィードのアイテムに表示されるすべての追加情報を指定します。
    
> [!TIP]
> アクティビティ フィードに表示されるアイコンは、常に、 **ISocialProvider::SocialNetworkIcon**プロパティによって返されるプロバイダーのアイコンと同じです。 
  
**ActivityDetails**要素、要素の**activityTemplateContainer** 、テンプレート トークン、およびテンプレート変数の詳細については次のトピックを参照してください。 
  
- [activityDetails 要素](activitydetails-element.md)
    
- [activityTemplateContainer 要素](activitytemplatecontainer-element.md)
    
- [テンプレート変数](template-variables.md)
    
- [アクティビティを正しく表示するためのガイドライン](guidelines-for-properly-displaying-activities.md)
    
アクティビティの例については、フィードの XML、[アクティビティ フィードの XML の例](activity-feed-xml-example.md)を参照してください。
  
## <a name="see-also"></a>関連項目

- [活動の XML](xml-for-activities.md) 
- [Outlook ソーシャル コネクタ プロバイダーの XML スキーマ](outlook-social-connector-provider-xml-schema.md)
- [OSC の XML スキーマを使用してプロバイダーの開発](developing-a-provider-with-the-osc-xml-schema.md)

