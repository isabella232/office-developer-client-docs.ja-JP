---
title: activitytemplatecontainer 要素
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 74662f25-5e18-4d0b-999c-a144427ad9e3
description: activitytemplatecontainer 要素は、アクティビティフィードアイテムを書式設定し、レイアウトを指定する XML を再利用できるテンプレートです。
ms.openlocfilehash: c2540b1d871e440e8f8f343a1788194c32d7dcc2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281121"
---
# <a name="activitytemplatecontainer-element"></a>activitytemplatecontainer 要素

**activitytemplatecontainer**要素は、アクティビティフィードアイテムを書式設定し、レイアウトを指定する XML を再利用できるテンプレートです。 id (**applicationID**および**templateID**) を使用して、フィードアイテム (**activitydetails**) をテンプレート (**activitytemplatecontainer**) と照合します。 レイアウトデータを**activitytemplate**要素の一部として格納します。 個別のアクティビティフィードアイテムから取り出されたデータを参照するには、人物、リンク、テキストなどの情報のためにテンプレート変数をプレースホルダーとして使用します。 
  
次の表では、 **activitytemplatecontainer**要素に必要な3つの要素について説明します。 
  
|**要素**|**説明**|
|:-----|:-----|
|**applicationID** <br/> |フィードアイテムとそのテンプレートを一致させるために使用される2つの一意の id のいずれか。 複数のアプリケーションまたは他のグループがある場合は、これを第1層のテンプレートオーガナイザーとして使用できます。  <br/> |
|**templateID** <br/> |フィードアイテムとそのテンプレートを照合するために使用される2番目の一意の ID。 これは、第2層のテンプレート開催者として使用できます。  <br/> |
|**activitytemplate** <br/> |テンプレートのレイアウト (**アイコン**、**タイトル**、**データ**要素)、およびアクティビティの種類 (**type**要素)。  <br/> |
   
次の表では、テンプレートのレイアウトと種類を説明する**activitytemplate**の子要素について説明します。
  
|**要素**|**説明**|
|:-----|:-----|
|**icon** <br/> |リンクトークン。そのフィードアイテムのアイコンの URL を参照します。  <br/> |
|**title** <br/> |フィードアイテムに必要な情報。  <br/> |
|**type** <br/> |状態、写真、ドキュメントの更新など、アクティビティの種類。  <br/> |
|**data** <br/> |フィードアイテムの追加情報 (画像、テキスト、リンクなど)。  <br/> |
   
アクティビティフィード xml の例については、「[アクティビティフィード xml の例](activity-feed-xml-example.md)」を参照してください。
  
## <a name="see-also"></a>関連項目

- [アクティビティフィードアイテムの XML の概要](overview-of-xml-for-an-activity-feed-item.md)  
- [activitydetails 要素](activitydetails-element.md)  
- [テンプレート変数](template-variables.md)  
- [アクティビティを適切に表示するためのガイドライン](guidelines-for-properly-displaying-activities.md)  
- [アクティビティの XML](xml-for-activities.md)  
- [Outlook Social Connector プロバイダーの XML スキーマ](outlook-social-connector-provider-xml-schema.md)
- [.osc XML スキーマを使用してプロバイダーを開発する](developing-a-provider-with-the-osc-xml-schema.md)

