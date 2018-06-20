---
title: 活動の XML
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: acc4a555-a3bf-4a79-86dc-aba6477733b8
description: このトピックには、Outlook ソーシャル コネクタ (OSC) プロバイダーに、OSC プロバイダーを実装し、OSC では、アクティビティの情報を取得する機能拡張 API の呼び出しを表示するシナリオ例にはが含まれています。 情報は、OSC プロバイダーの XML スキーマに準拠する XML 文字列で表されます。
ms.openlocfilehash: 44f74d9e72eec3ff6da7f9967315fc9d75191584
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804475"
---
# <a name="xml-for-activities"></a>活動の XML

このトピックには、Outlook ソーシャル コネクタ (OSC) プロバイダーに、OSC プロバイダーを実装し、OSC では、アクティビティの情報を取得する機能拡張 API の呼び出しを表示するシナリオ例にはが含まれています。 情報は、OSC プロバイダーの XML スキーマに準拠する XML 文字列で表されます。
  
OSC プロバイダーの XML スキーマでは、アクティビティを定義するのには、OSC プロバイダーを許可します。 活動の情報は、ソーシャル ネットワーク アクティビティが発生した場合、アイテムをフィードごとのアクティビティ フィードのアイテムの詳細を含めることができます (などの所有者は、入力、発行とアクティビティの日付)、および活動を表示するテンプレートです。 人物情報ウィンドウまたは連絡先カードに表示されているアクティビティをサポートするためにソーシャル ネットワークの OSC プロバイダーが実装し、正しい活動の XML を返す必要があります。 アクティビティの例については、フィードの XML、[アクティビティ フィードの XML の例](activity-feed-xml-example.md)を参照してください。 友人の活動を同期の詳細については、[同期の友人との活動](synchronizing-friends-and-activities.md)を参照してください。 のどの要素には、必須またはオプションを含む、OSC プロバイダーの XML スキーマの完全な定義は、 [Outlook ソーシャル コネクタ プロバイダーの XML スキーマ](outlook-social-connector-provider-xml-schema.md)を参照してください。 
  
次のシナリオでは、OSC は動的に、人物情報ウィンドウで選択されているユーザーのアクティビティを同期し、そのユーザーに関する詳細情報を取得します。
  
1. OSC プロバイダーのアクティビティのオン ・ デマンドの同期をサポートすることを示します、OSC に、 **getActivities**と**dynamicActivitiesLookupEx**の要素を使用しています。 OSC プロバイダーも**実装しています。** 要素を設定します。 3 つすべての要素は、**機能**の子要素です。 
    
2. OSC プロバイダーは、 **ISocialProvider::GetCapabilities**メソッドと[ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md)メソッドを実装します。 
    
3. **GetActivities**および**dynamicActivitiesLookupEx**の値を確認するために、OSC プロバイダー OSC **ISocialProvider::GetCapabilities**の呼び出しには、活動のオン ・ デマンドの同期がサポートされています。 OSC では、OSC プロバイダーでサポートされている**実装しています。** 要素の値もメモします。 
    
4. OSC では、ユーザーが選択したユーザーの最新の活動を確認できるようにするには、人物情報ウィンドウまたは連絡先カードを更新します。 OSC は、 **hashedAddresses**要素の XML スキーマ定義に準拠する XML 文字列を形成する、**実装しています。** 要素で指定されているハッシュ関数を使用してユーザーの SMTP アドレスを暗号化します。 
    
5. OSC では、 **ISocialSession2::GetActivitiesEx**、 _hashedAddresses_のパラメーターとして、ハッシュ化されたアドレスの場合は、この XML 文字列を提供する_活動_のパラメーターでは、その人の活動の現在のコレクションを取得するを呼び出します。 _アクティビティ_パラメーター文字列は、 **activityFeed**要素の XML スキーマ定義に準拠します。 
    
6. **ActivityFeed**の XML スキーマ定義に基づき、OSC をさらには、型を調べるには、日付、およびそれぞれの活動に関するその他の情報およびアクティビティを表示する方法を公開_活動_文字列を解析します。 
    
7. OSC は、選択したユーザーに関する詳細情報を取得するには、 [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md)、 _personsAddresses_パラメーターの引数として、同じ XML 文字列をハッシュ化されたアドレスを提供することを呼び出します。 _PersonsCollection_パラメーターでは、ユーザーに関する詳細な情報が返されます。 これらの詳細については、**姓****姓**、および**emailAddress**を含めることができます。 _PersonsCollection_パラメーターは、**人**の要素の XML スキーマ定義に準拠しています。 
    
アクティビティのこのセクションの以下のトピックで、XML を指定する方法の詳細をご覧ください。
  
- [フィード アイテムの活動項目の XML の概要](overview-of-xml-for-an-activity-feed-item.md)
    
- [activityDetails 要素](activitydetails-element.md)
    
- [activityTemplateContainer 要素](activitytemplatecontainer-element.md)
    
- [テンプレート変数](template-variables.md)
    
- [アクティビティを正しく表示するためのガイドライン](guidelines-for-properly-displaying-activities.md)
    
## <a name="see-also"></a>関連項目

- [アクティビティ フィードの XML の例](activity-feed-xml-example.md)  
- [友人や活動を同期します。](synchronizing-friends-and-activities.md) 
- [機能のための XML](xml-for-capabilities.md)  
- [友人の XML](xml-for-friends.md)
- [OSC の XML スキーマを使用してプロバイダーの開発](developing-a-provider-with-the-osc-xml-schema.md)

