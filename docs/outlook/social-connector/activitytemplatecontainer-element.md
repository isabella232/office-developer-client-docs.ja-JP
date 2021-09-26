---
title: activityTemplateContainer 要素
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 74662f25-5e18-4d0b-999c-a144427ad9e3
description: activityTemplateContainer 要素は、アクティビティ フィード アイテムの書式を設定し、レイアウトを指定する XML を再利用できるテンプレートです。
ms.openlocfilehash: 7b0d8e8d995721e3a58b3b0db1bb7b403be445dc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583052"
---
# <a name="activitytemplatecontainer-element"></a>activityTemplateContainer 要素

**activityTemplateContainer** 要素は、アクティビティ フィード アイテムの書式を設定し、レイアウトを指定する XML を再利用できるテンプレートです。 フィード アイテム (**activityDetails**) をテンプレート (**activityTemplateContainer**) に一致するには、ID (**applicationID** と **templateID**) を使用します。 レイアウト データを **activityTemplate 要素の一部として格納** します。 個々のアクティビティ フィード アイテムから取得されたデータを参照するには、ユーザー、リンク、テキストなどの情報のプレースホルダーとしてテンプレート変数を使用します。 
  
次の表に **、activityTemplateContainer** 要素で必要な 3 つの要素について説明します。 
  
|**Element**|**説明**|
|:-----|:-----|
|**applicationID** <br/> |フィード アイテムとテンプレートを一致するために使用される 2 つの一意の ID の 1 つ。 複数のアプリケーションまたは他のグループ化がある場合、これは第 1 層テンプレートオーガナイザーとして使用できます。  <br/> |
|**templateID** <br/> |フィード アイテムとテンプレートを一致するために使用される 2 番目の一意の ID。 これは、第 2 層テンプレートオーガナイザーとして使用できます。  <br/> |
|**activityTemplate** <br/> |テンプレートのレイアウト (**アイコン**、**タイトル、および****データ** 要素)、およびアクティビティの種類 (**型** 要素)。  <br/> |
   
次の表では、レイアウトとテンプレートの種類を説明する **activityTemplate** の子要素について説明します。
  
|**Element**|**説明**|
|:-----|:-----|
|**icon** <br/> |そのフィード アイテムのアイコンの URL を参照するリンク トークン。  <br/> |
|**title** <br/> |フィード アイテムに必要な情報。  <br/> |
|**type** <br/> |アクティビティの種類 (ステータス、写真、ドキュメントの更新など)。  <br/> |
|**data** <br/> |画像、テキスト、リンクなど、フィード アイテムに関する追加情報。  <br/> |
   
アクティビティ フィード XML の例については、「アクティビティ フィード [XML の例」を参照してください。](activity-feed-xml-example.md)
  
## <a name="see-also"></a>関連項目

- [アクティビティ フィード アイテムの XML の概要](overview-of-xml-for-an-activity-feed-item.md)  
- [activityDetails 要素](activitydetails-element.md)  
- [テンプレート変数](template-variables.md)  
- [アクティビティを適切に表示するためのガイドライン](guidelines-for-properly-displaying-activities.md)  
- [アクティビティの XML](xml-for-activities.md)  
- [Outlookソーシャル コネクタ プロバイダー XML スキーマ](outlook-social-connector-provider-xml-schema.md)
- [OSC XML スキーマを使用したプロバイダーの開発](developing-a-provider-with-the-osc-xml-schema.md)

