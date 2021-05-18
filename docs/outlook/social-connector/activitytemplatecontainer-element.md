---
title: activityTemplateContainer 要素
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 74662f25-5e18-4d0b-999c-a144427ad9e3
description: activityTemplateContainer 要素は、アクティビティ フィード アイテムの書式を設定し、レイアウトを指定する XML を再利用できるテンプレートです。
ms.openlocfilehash: c2540b1d871e440e8f8f343a1788194c32d7dcc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413718"
---
# <a name="activitytemplatecontainer-element"></a>activityTemplateContainer 要素

**activityTemplateContainer** 要素は、アクティビティ フィード アイテムの書式を設定し、レイアウトを指定する XML を再利用できるテンプレートです。 フィード アイテム (**activityDetails**) をテンプレート (**activityTemplateContainer**) に一致するには、ID (**applicationID** と **templateID**) を使用します。 レイアウト データを **activityTemplate 要素の一部として格納** します。 個々のアクティビティ フィード アイテムから取得されたデータを参照するには、ユーザー、リンク、テキストなどの情報のプレースホルダーとしてテンプレート変数を使用します。 
  
次の表に **、activityTemplateContainer** 要素で必要な 3 つの要素について説明します。 
  
|**要素**|**説明**|
|:-----|:-----|
|**applicationID** <br/> |フィード アイテムとテンプレートを一致するために使用される 2 つの一意の ID の 1 つ。 複数のアプリケーションまたは他のグループ化がある場合、これは第 1 層テンプレートオーガナイザーとして使用できます。  <br/> |
|**templateID** <br/> |フィード アイテムとテンプレートを一致するために使用される 2 番目の一意の ID。 これは、第 2 層テンプレートオーガナイザーとして使用できます。  <br/> |
|**activityTemplate** <br/> |テンプレートのレイアウト (**アイコン**、**タイトル、および****データ** 要素)、およびアクティビティの種類 (**型** 要素)。  <br/> |
   
次の表では、レイアウトとテンプレートの種類を説明する **activityTemplate** の子要素について説明します。
  
|**要素**|**説明**|
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

