---
title: activityDetails 要素
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c103d48d-53ca-4b19-b16f-2862379587ef
description: ActivityDetails 要素は、1 つのアクティビティ フィードのアイテム用の生データを格納します。 各アクティビティのフィードのアイテムには、独自の activityDetails 要素が必要です。 ActivityDetails 要素内のデータは、名前の要素を使用して、アクティビティ テンプレートで参照されます。
ms.openlocfilehash: c326017a038dff138d690b020a98972a08212690
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804333"
---
# <a name="activitydetails-element"></a>activityDetails 要素

**ActivityDetails**要素は、1 つのアクティビティ フィードのアイテム用の生データを格納します。 各アクティビティのフィードのアイテムには、独自の**activityDetails**要素が必要です。 **ActivityDetails**要素内のデータは、**名前**の要素を使用して、アクティビティ テンプレートで参照されます。 **ActivityDetails**要素内のデータの各要素には、 **name**要素が必要です。 
  
次の表では、 **activityDetails**要素を必要とする 6 つの要素について説明します。 
  
|**要素**|**説明**|
|:-----|:-----|
|**ownerID** <br/> |この活動を生成したソーシャル ネットワーク上のユーザーの ID は、アイテムをフィードします。  <br/> |
|**オブジェクト Id** <br/> |アクティビティの一意の文字列では、フィード アイテムの重複を検出するために項目をフィードします。  <br/> |
|**applicationId** <br/> |アクティビティを一致するように使用される 2 つの一意の Id のいずれかのフィードの項目テンプレートを使用します。 複数のアプリケーションまたはその他のグループがあれば、1 層構成のテンプレートの開催者は、これを使用できます。  <br/> |
|**templateId** <br/> |アクティビティを一致させるために使用される 2 つ目の一意の ID は、そのテンプレートを使用してアイテムをフィードします。 開催者は、第 2 層のテンプレートは、これを使用できます。  <br/> |
|**publishDate** <br/> |日付と時間、アクティビティ フィードのアイテムを発行します。  <br/> |
|**templateVariables** <br/> |アクティビティ フィード項目テンプレートのトークンに使用するデータ。  <br/> |
   
アクティビティの例については、フィードの XML、[アクティビティ フィードの XML の例](activity-feed-xml-example.md)を参照してください。
  
## <a name="see-also"></a>関連項目

- [フィード アイテムの活動項目の XML の概要](overview-of-xml-for-an-activity-feed-item.md)  
- [activityTemplateContainer 要素](activitytemplatecontainer-element.md)  
- [テンプレート変数](template-variables.md) 
- [アクティビティを正しく表示するためのガイドライン](guidelines-for-properly-displaying-activities.md)  
- [活動の XML](xml-for-activities.md)  
- [Outlook ソーシャル コネクタ プロバイダーの XML スキーマ](outlook-social-connector-provider-xml-schema.md)
- [OSC の XML スキーマを使用してプロバイダーの開発](developing-a-provider-with-the-osc-xml-schema.md)

