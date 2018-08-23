---
title: activityTemplateContainer 要素
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 74662f25-5e18-4d0b-999c-a144427ad9e3
description: ActivityTemplateContainer 要素は、テンプレート、アクティビティ フィードのアイテムの書式設定し、レイアウトを指定する XML を再利用するためです。
ms.openlocfilehash: e744bb1bdb828003cdda7086468533b32b4bf20f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804336"
---
# <a name="activitytemplatecontainer-element"></a>activityTemplateContainer 要素

**ActivityTemplateContainer**要素は、テンプレート、アクティビティ フィードのアイテムの書式設定し、レイアウトを指定する XML を再利用するためです。 Id (**付きアプリケーション Id** **テンプレート Id**) テンプレート (**activityTemplateContainer**) へのフィードのアイテム (**activityDetails**) と一致するを使用します。 **ActivityTemplate**要素の一部としてレイアウトのデータを格納します。 個々 のアクティビティのフィードのアイテムから抽出されたデータを参照するには、人、リンク、およびテキストなどの情報のプレース ホルダーとしてテンプレート変数を使用します。 
  
次の表では、 **activityTemplateContainer**要素を必要とする 3 つの要素について説明します。 
  
|**要素**|**説明**|
|:-----|:-----|
|**付きアプリケーション Id** <br/> |そのテンプレートを使用してフィードの項目に一致するように使用される 2 つの一意の Id の 1 つです。 複数のアプリケーションまたはその他のグループがあれば、1 層構成のテンプレートの開催者は、これを使用できます。  <br/> |
|**テンプレート Id** <br/> |そのテンプレートを使用してフィードの項目を一致させるために使用される 2 番目の固有 ID。 開催者は、第 2 層のテンプレートは、これを使用できます。  <br/> |
|**activityTemplate** <br/> |テンプレート (**アイコン**、**タイトル**、および**データ**要素) と活動 (**型**の要素) の種類のレイアウト。  <br/> |
   
次の表では、レイアウトとテンプレートの種類を説明する**activityTemplate**の子要素について説明します。
  
|**要素**|**説明**|
|:-----|:-----|
|**icon** <br/> |そのフィードのアイテムのアイコンの URL を参照するリンク トークンです。  <br/> |
|**title** <br/> |フィードの項目に必要な情報です。  <br/> |
|**type** <br/> |状態、写真、またはドキュメントの更新など、活動の種類。  <br/> |
|**data** <br/> |フィード項目、画像、テキスト、リンクなどの追加情報です。  <br/> |
   
アクティビティの例については、フィードの XML、[アクティビティ フィードの XML の例](activity-feed-xml-example.md)を参照してください。
  
## <a name="see-also"></a>関連項目

- [フィード アイテムの活動項目の XML の概要](overview-of-xml-for-an-activity-feed-item.md)  
- [activityDetails 要素](activitydetails-element.md)  
- [テンプレート変数](template-variables.md)  
- [アクティビティを正しく表示するためのガイドライン](guidelines-for-properly-displaying-activities.md)  
- [活動の XML](xml-for-activities.md)  
- [Outlook ソーシャル コネクタ プロバイダーの XML スキーマ](outlook-social-connector-provider-xml-schema.md)
- [OSC の XML スキーマを使用してプロバイダーの開発](developing-a-provider-with-the-osc-xml-schema.md)

