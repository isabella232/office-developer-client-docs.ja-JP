---
title: アクティビティを正しく表示するためのガイドライン
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 55268188-8432-4145-9527-f5888949fc24
description: Outlook ソーシャル コネクタ (OSC) プロバイダーには、OSC の活動項目をメモリに格納する getActivities と dynamicActivitiesLookupEx の要素を設定できます。
ms.openlocfilehash: f8cb5850c8920f09f784343db18372bb75ca17a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804331"
---
# <a name="guidelines-for-properly-displaying-activities"></a>アクティビティを正しく表示するためのガイドライン

Outlook ソーシャル コネクタ (OSC) のプロバイダーは、 **getActivities**を設定でき、OSC に**dynamicActivitiesLookupEx**要素は、活動項目をメモリに格納します。 OSC プロバイダーは、同期アクティビティをサポートしている場合を取得またはアクティビティおよびアクティビティの所有者の詳細を更新するには、OSC を呼び出す Api のフィードをソーシャル ネットワークから、OSC プロバイダーの機能拡張について説明します。 OSC プロバイダーは、連絡先カードの Office または Outlook 人物情報ウィンドウでのアクティビティを正しく表示するための OSC の設定をする必要があります**activityFeed**要素のいくつかの子要素についても説明します。 
  
- OSC では、取得し、ニュース フィードのフォルダーにログオンしているユーザーのアクティビティを格納する[ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md)メソッドを呼び出します。 OSC プロバイダーは、OSC プロバイダーの**activityFeed**要素の XML スキーマ定義に準拠している_アクティビティ_の XML 文字列を返すには、 **GetActivitiesEx**を実装しなければなりません。 
    
- OSC プロバイダーでは、 **activityDetails**要素の子要素である、 **ownerID**要素を設定する必要があります。 **ownerID**は、不透明なソーシャル ネットワーク上の活動の所有者を識別する文字列です。 
    
- OSC プロバイダーは、 **templateVariables**要素の [ **publisherVariable** ] ノードで、 **nameHint**と**emailAddress**要素を設定する必要があります。 
    
   OSC プロバイダーの XML スキーマでは、各**nameHint**の要素が省略可能な要素に注意してください。 OSC では、連絡先カードまたは人物情報ウィンドウで選択したユーザーの表示名を一致するようにそれを使用します。 同様に、 **emailAddress**要素は、XML スキーマに省略可能な要素です。 OSC では、連絡先カードまたは人物情報ウィンドウで選択したユーザーの SMTP アドレスと一致するのに、それを使用します。 
    
   [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md)メソッドとし、 [ISocialPerson::GetDetails](isocialperson-getdetails.md) OSC を呼び出す場合だけ**ownerID**要素を指定すると、 **nameHint**および**emailAddress**の一方または両方が指定されていない、**ownerID**によって識別されるユーザーに関する詳細情報を取得するメソッドです。 OSC が**ISocialPerson::GetDetails**を呼び出すと、プロバイダーは**人****氏名**と**emailAddress**要素を指定する XML を返す必要があります。 
    
## <a name="see-also"></a>関連項目

- [活動の XML](xml-for-activities.md)  
- [友人の XML](xml-for-friends.md)  
- [機能のための XML](xml-for-capabilities.md)

