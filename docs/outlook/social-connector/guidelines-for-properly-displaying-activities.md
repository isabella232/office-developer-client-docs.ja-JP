---
title: アクティビティを正しく表示するためのガイドライン
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 55268188-8432-4145-9527-f5888949fc24
description: Outlookソーシャル コネクタ (OSC) プロバイダーは、getActivities 要素と dynamicActivitiesLookupEx 要素を設定して、OSC にアクティビティ アイテムをメモリに格納できます。
ms.openlocfilehash: b2fcaa125ac8bf7924726f4f09ff507769c3a3f7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422916"
---
# <a name="guidelines-for-properly-displaying-activities"></a>アクティビティを正しく表示するためのガイドライン

Outlookソーシャル コネクタ (OSC) プロバイダーは **、getActivities** 要素と **dynamicActivitiesLookupEx** 要素を設定して、OSC にアクティビティ アイテムをメモリに格納できます。 このトピックでは、OSC プロバイダーがソーシャル ネットワークからのアクティビティ フィードの同期をサポートしている場合に、OSC がアクティビティとアクティビティ所有者の詳細を取得または更新するために呼び出す OSC プロバイダー拡張 API について説明します。 また、OSC プロバイダーが Office 連絡先カードまたは Outlook People Pane でアクティビティを適切に表示するために OSC プロバイダーが設定する **activityFeed** 要素のいくつかの子要素も一覧表示します。 
  
- OSC は [、ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) メソッドを呼び出して、ログオンしているユーザーのニュース フィード フォルダーにアクティビティを取得して保存します。 OSC プロバイダーは **GetActivitiesEx** を実装して **、activityFeed** 要素の OSC プロバイダー XML スキーマ定義に準拠するアクティビティ XML 文字列を返す必要があります。 
    
- OSC プロバイダーは **、activityDetails** 要素の子要素である **ownerID** 要素を設定する必要があります。 **ownerID** は、ソーシャル ネットワーク上のアクティビティの所有者を識別する不透明な文字列です。 
    
- OSC プロバイダーは **、templateVariables** 要素の **publisherVariable** ノードで nameHint 要素と **emailAddress** 要素 **を設定する必要** があります。 
    
   OSC プロバイダー XML スキーマごとに **、nameHint** 要素は省略可能な要素です。 OSC は、連絡先カードまたはユーザー ウィンドウで選択したユーザーの表示名と一致するために使用します。 同様に **、emailAddress** 要素は XML スキーマの省略可能な要素です。 OSC は、連絡先カードまたはユーザー ウィンドウで選択したユーザーの SMTP アドレスと一致するために使用します。 
    
   ownerID要素のみを指定したが **、nameHint** と **emailAddress** の一方または両方が指定されていない場合、OSC は [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md)メソッドを呼び出し、次に [ISocialPerson::GetDetails](isocialperson-getdetails.md)メソッドを呼び出して **、ownerID** で識別された人物に関する詳細な情報を取得します。 OSC が **ISocialPerson::GetDetails** を呼び出す場合、プロバイダーは **fullName** 要素と **emailAddress** 要素を指定するユーザー **XML** を返す必要があります。 
    
## <a name="see-also"></a>関連項目

- [アクティビティの XML](xml-for-activities.md)  
- [友人のための XML](xml-for-friends.md)  
- [機能の XML](xml-for-capabilities.md)

