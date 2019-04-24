---
title: アクティビティ用 XML
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: acc4a555-a3bf-4a79-86dc-aba6477733b8
description: このトピックには、アクティビティ情報を取得するために、.osc プロバイダーが実装する Outlook Social Connector (.osc) プロバイダーの機能拡張 API 呼び出しを示すシナリオの例が含まれています。 情報は、.osc プロバイダ xml スキーマに準拠する xml 文字列で表されます。
ms.openlocfilehash: a4f1c6ce1f33b59811f6a6fecb737cd1f737946b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329121"
---
# <a name="xml-for-activities"></a>アクティビティ用 XML

このトピックには、アクティビティ情報を取得するために、.osc プロバイダーが実装する Outlook Social Connector (.osc) プロバイダーの機能拡張 API 呼び出しを示すシナリオの例が含まれています。 情報は、.osc プロバイダ xml スキーマに準拠する xml 文字列で表されます。
  
.osc プロバイダ XML スキーマを使用すると、.osc プロバイダーはアクティビティを定義できます。 アクティビティ情報には、アクティビティフィードアイテムが送信されたソーシャルネットワーク、各アクティビティフィードアイテムの詳細 (アクティビティの所有者、種類、発行日など)、およびアクティビティを表示するためのテンプレートが含まれます。 ユーザーウィンドウまたは連絡先カードでのアクティビティの表示をサポートするには、ソーシャルネットワークの .osc プロバイダーが適切なアクティビティ XML を実装して返す必要があります。 アクティビティフィード xml の例については、「[アクティビティフィード xml の例](activity-feed-xml-example.md)」を参照してください。 フレンドのアクティビティの同期の詳細については、「[友人とアクティビティを同期](synchronizing-friends-and-activities.md)する」を参照してください。 必要な要素やオプションの要素を含む、.osc プロバイダ XML スキーマの完全な定義については、「 [Outlook Social Connector プロバイダーの xml スキーマ](outlook-social-connector-provider-xml-schema.md)」を参照してください。 
  
次のシナリオでは、[人] ウィンドウで選択したユーザーのアクティビティを、.osc が動的に同期し、その人物に関する詳細を取得します。
  
1. アクティビティのオンデマンド同期をサポートする .osc プロバイダーは、getactivities 要素と**dynamicActivitiesLookupEx**要素を使用**** して、.osc に対してを指定します。 .osc プロバイダーは、 **hashfunction**要素も設定します。 3つすべての要素は、**機能**の子要素です。 
    
2. .osc プロバイダーは、 **iISocialSession2 alprovider:: getcapabilities**メソッドと[:: GetActivitiesEx](isocialsession2-getactivitiesex.md)メソッドを実装します。 
    
3. .osc は**idynamicActivitiesLookupEx alprovider:: getcapabilities**を呼び出して、.osc プロバイダー **** がアクティビティの**** オンデマンド同期をサポートしているかどうかを確認します。 .osc は、.osc プロバイダーでサポートされている**hashfunction**要素の値もメモします。 
    
4. .osc は、ユーザーウィンドウまたは連絡先カードを更新して、選択されている人物の最新のアクティビティをユーザーに表示できるようにします。 .osc は、 **hashfunction**要素で指定されたハッシュ関数を使用して、その人物の SMTP アドレスを暗号化し、 **hashedAddresses**要素の xml スキーマ定義に準拠した xml 文字列を形成します。 
    
5. .osc は**ISocialSession2:: GetActivitiesEx**を呼び出して、ハッシュ化されたアドレスのこの XML 文字列を_hashedAddresses_パラメーターとして提供し、その人物の現在のアクティビティのコレクションを_交際_パラメーターで取得します。 _アクティビティ_パラメーター文字列は、 **activityfeed**要素の XML スキーマ定義に準拠しています。 
    
6. アクティビティ**フィード**の XML スキーマ定義に基づいて、_アクティビティ_文字列をさらに解析して、各アクティビティに関する型、発行日、その他の情報を見つけ、アクティビティを表示する方法を示します。 
    
7. 選択した人物に関する詳細を取得するために、.osc は[ISocialSession2:: GetPeopleDetails](isocialsession2-getpeopledetails.md)を呼び出し、ハッシュされたアドレスの同じ XML 文字列を、_個人_情報パラメーターの引数として提供します。 個人に関する詳細は、個人_コレクション_パラメーターで返されます。 これらの詳細には、 **firstName**、 **lastName**、 **emailAddress**を含めることができます。 個人_コレクション_パラメーターは、 **person**要素の XML スキーマ定義に準拠しています。 
    
アクティビティの XML を指定する方法の詳細については、このセクションの次のトピックを参照してください。
  
- [アクティビティフィードアイテムの XML の概要](overview-of-xml-for-an-activity-feed-item.md)
    
- [activitydetails 要素](activitydetails-element.md)
    
- [activitytemplatecontainer 要素](activitytemplatecontainer-element.md)
    
- [テンプレート変数](template-variables.md)
    
- [アクティビティを適切に表示するためのガイドライン](guidelines-for-properly-displaying-activities.md)
    
## <a name="see-also"></a>関連項目

- [アクティビティフィード XML の例](activity-feed-xml-example.md)  
- [フレンドとアクティビティの同期](synchronizing-friends-and-activities.md) 
- [機能の XML](xml-for-capabilities.md)  
- [Friends の XML](xml-for-friends.md)
- [.osc XML スキーマを使用してプロバイダーを開発する](developing-a-provider-with-the-osc-xml-schema.md)

