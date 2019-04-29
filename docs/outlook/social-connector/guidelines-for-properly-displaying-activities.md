---
title: アクティビティを正しく表示するためのガイドライン
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 55268188-8432-4145-9527-f5888949fc24
description: Outlook Social Connector (.osc) プロバイダーは、getactivities および dynamicActivitiesLookupEx 要素が、.osc store アクティビティアイテムをメモリに保持するように設定できます。
ms.openlocfilehash: b2fcaa125ac8bf7924726f4f09ff507769c3a3f7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422916"
---
# <a name="guidelines-for-properly-displaying-activities"></a>アクティビティを正しく表示するためのガイドライン

Outlook Social Connector (.osc) プロバイダーは、 **getactivities**および**dynamicActivitiesLookupEx**要素が、.osc store アクティビティアイテムをメモリに保持するように設定できます。 このトピックでは、.osc プロバイダーがソーシャルネットワークからのアクティビティフィードの同期をサポートしている場合に、アクティビティとアクティビティ所有者の詳細を取得または更新するために、.osc が呼び出すプロバイダー拡張 api について説明します。 また、このトピックには、.osc に対して .osc プロバイダーで設定する必要がある**activityfeed**要素のいくつかの子要素が表示されます。これにより、Office の連絡先カードまたは Outlook の [ユーザー] ウィンドウにアクティビティが適切に表示されます。 
  
- .osc は、 [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md)メソッドを呼び出して、ログオンしているユーザーのニュースフィードフォルダーにアクティビティを取得して保存します。 .osc プロバイダーは、 **GetActivitiesEx**を実装して、 **activityfeed**要素の .osc プロバイダ xml スキーマ定義に準拠した_アクティビティ_xml 文字列を返す必要があります。 
    
- .osc プロバイダーは、 **activitydetails**要素の子要素である**ownerID**要素を設定する必要があります。 **ownerID**は、ソーシャルネットワーク上のアクティビティの所有者を識別する非透過文字列です。 
    
- .osc プロバイダーは、 **templateVariables**要素の**publisherVariable**ノードで**namehint**および**emailAddress**要素を設定する必要があります。 
    
   .osc プロバイダーの XML スキーマの場合、 **namehint**要素は省略可能な要素であることに注意してください。 .osc は、これを使用して、連絡先カードまたは [ユーザー] ウィンドウで選択したユーザーの表示名と照合します。 同様に、 **emailAddress**要素は、XML スキーマの省略可能な要素です。 .osc は、連絡先カードまたはユーザーウィンドウで選択したユーザーの SMTP アドレスと一致するように使用します。 
    
   **ownerID**要素のみが指定されていて、 **namehint**と**emailAddress**の一方または両方が指定されていない場合、.osc は[ISocialSession2:: GetPeopleDetails](isocialsession2-getpeopledetails.md)メソッドを呼び出した後、 [i alperson:: getdetails](isocialperson-getdetails.md)を呼び出します。メソッドを使って、 **ownerID**によって識別される個人に関する詳細情報を取得します。 .osc が iemailAddress **alperson:: getdetails**を呼び出した場合、プロバイダーは**fullName**要素と**** 要素を指定する**person** XML を返す必要があります。 
    
## <a name="see-also"></a>関連項目

- [アクティビティの XML](xml-for-activities.md)  
- [Friends の XML](xml-for-friends.md)  
- [機能の XML](xml-for-capabilities.md)

