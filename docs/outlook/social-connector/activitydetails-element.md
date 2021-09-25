---
title: activityDetails 要素
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: c103d48d-53ca-4b19-b16f-2862379587ef
description: activityDetails 要素は、1 つのアクティビティ フィード アイテムの生データを格納します。 各アクティビティ フィード アイテムには、独自の activityDetails 要素が必要です。 activityDetails 要素のデータは、name 要素を使用してアクティビティ テンプレートで参照されます。
ms.openlocfilehash: a9249f3480d1cd72b01d52af15a843bb88b4625f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629173"
---
# <a name="activitydetails-element"></a>activityDetails 要素

**activityDetails 要素** は、1 つのアクティビティ フィード アイテムの生データを格納します。 各アクティビティ フィード アイテムには、独自の **activityDetails 要素が必要** です。 **activityDetails 要素のデータ** は、name 要素を使用してアクティビティ テンプレート **で参照** されます。 **activityDetails** 要素のすべてのデータには、name 要素が **必要** です。 
  
次の表に **、activityDetails** 要素で必要な 6 つの要素について説明します。 
  
|**Element**|**説明**|
|:-----|:-----|
|**ownerID** <br/> |このアクティビティ フィード アイテムを生成したソーシャル ネットワーク上のユーザーの ID。  <br/> |
|**objectID** <br/> |重複するフィード アイテムを検出するアクティビティ フィード アイテムの一意の文字列。  <br/> |
|**applicationId** <br/> |アクティビティ フィード アイテムとテンプレートを一致するために使用される 2 つの一意の ID の 1 つ。 複数のアプリケーションまたは他のグループ化がある場合、これは第 1 層テンプレートオーガナイザーとして使用できます。  <br/> |
|**templateId** <br/> |アクティビティ フィード アイテムとテンプレートを一致するために使用される 2 番目の一意の ID。 これは、第 2 層テンプレートオーガナイザーとして使用できます。  <br/> |
|**publishDate** <br/> |アクティビティ フィード アイテムが発行された日付と時刻。  <br/> |
|**templateVariables** <br/> |アクティビティ フィード アイテム テンプレートのトークンで使用するデータ。  <br/> |
   
アクティビティ フィード XML の例については、「アクティビティ フィード [XML の例」を参照してください。](activity-feed-xml-example.md)
  
## <a name="see-also"></a>関連項目

- [アクティビティ フィード アイテムの XML の概要](overview-of-xml-for-an-activity-feed-item.md)  
- [activityTemplateContainer 要素](activitytemplatecontainer-element.md)  
- [テンプレート変数](template-variables.md) 
- [アクティビティを適切に表示するためのガイドライン](guidelines-for-properly-displaying-activities.md)  
- [アクティビティの XML](xml-for-activities.md)  
- [Outlookソーシャル コネクタ プロバイダー XML スキーマ](outlook-social-connector-provider-xml-schema.md)
- [OSC XML スキーマを使用したプロバイダーの開発](developing-a-provider-with-the-osc-xml-schema.md)

