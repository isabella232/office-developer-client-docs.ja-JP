---
title: activitydetails 要素
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c103d48d-53ca-4b19-b16f-2862379587ef
description: activitydetails 要素は、1つのアクティビティフィードアイテムの生データを格納します。 各アクティビティフィードアイテムは、独自の activitydetails 要素を持つ必要があります。 activitydetails 要素のデータは、アクティビティテンプレートで name 要素を使用して参照されます。
ms.openlocfilehash: fd9c2136e8e2b687fa281ecda71039809848f63c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434873"
---
# <a name="activitydetails-element"></a>activitydetails 要素

**activitydetails**要素は、1つのアクティビティフィードアイテムの生データを格納します。 各アクティビティフィードアイテムは、独自の**activitydetails**要素を持つ必要があります。 **activitydetails**要素のデータは、アクティビティテンプレートで**name**要素を使用して参照されます。 **activitydetails**要素のすべてのデータに**name**要素が含まれている必要があります。 
  
次の表では、 **activitydetails**要素に必要な6つの要素について説明します。 
  
|**要素**|**説明**|
|:-----|:-----|
|**ownerID** <br/> |このアクティビティフィードアイテムを生成したソーシャルネットワーク上のユーザーの ID。  <br/> |
|**id** <br/> |重複したフィードアイテムを検出するためのアクティビティフィードアイテムの一意の文字列。  <br/> |
|**applicationId** <br/> |アクティビティフィードアイテムをテンプレートと照合するために使用される2つの一意の id のいずれか。 複数のアプリケーションまたは他のグループがある場合は、これを第1層のテンプレートオーガナイザーとして使用できます。  <br/> |
|**templateId** <br/> |アクティビティフィードアイテムをテンプレートと照合するために使用される2番目の一意の ID。 これは、第2層のテンプレート開催者として使用できます。  <br/> |
|**publishdate** <br/> |アクティビティフィードアイテムが発行された日時。  <br/> |
|**templateVariables** <br/> |アクティビティフィードアイテムテンプレートのトークンで使用されるデータ。  <br/> |
   
アクティビティフィード xml の例については、「[アクティビティフィード xml の例](activity-feed-xml-example.md)」を参照してください。
  
## <a name="see-also"></a>関連項目

- [アクティビティフィードアイテムの XML の概要](overview-of-xml-for-an-activity-feed-item.md)  
- [activitytemplatecontainer 要素](activitytemplatecontainer-element.md)  
- [テンプレート変数](template-variables.md) 
- [アクティビティを適切に表示するためのガイドライン](guidelines-for-properly-displaying-activities.md)  
- [アクティビティの XML](xml-for-activities.md)  
- [Outlook Social Connector プロバイダーの XML スキーマ](outlook-social-connector-provider-xml-schema.md)
- [.osc XML スキーマを使用してプロバイダーを開発する](developing-a-provider-with-the-osc-xml-schema.md)

