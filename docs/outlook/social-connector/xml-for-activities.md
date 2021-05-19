---
title: アクティビティ用 XML
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: acc4a555-a3bf-4a79-86dc-aba6477733b8
description: このトピックでは、OSC プロバイダーが実装する Outlook Social Connector (OSC) プロバイダー拡張 API 呼び出しと、OSC がアクティビティ情報を取得するために行う呼び出しを示すシナリオの例を示します。 情報は、OSC プロバイダー XML スキーマに準拠した XML 文字列で表されます。
ms.openlocfilehash: a4f1c6ce1f33b59811f6a6fecb737cd1f737946b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409630"
---
# <a name="xml-for-activities"></a>アクティビティ用 XML

このトピックでは、OSC プロバイダーが実装する Outlook Social Connector (OSC) プロバイダー拡張 API 呼び出しと、OSC がアクティビティ情報を取得するために行う呼び出しを示すシナリオの例を示します。 情報は、OSC プロバイダー XML スキーマに準拠した XML 文字列で表されます。
  
OSC プロバイダーの XML スキーマを使用すると、OSC プロバイダーはアクティビティを定義できます。 アクティビティ情報には、アクティビティ フィード アイテムが発生したソーシャル ネットワーク、各アクティビティ フィード アイテムの詳細 (アクティビティの所有者、種類、発行日など)、アクティビティを表示するテンプレートが含まれます。 People Pane または Contact Card でのアクティビティの表示をサポートするには、ソーシャル ネットワークの OSC プロバイダーが正しいアクティビティ XML を実装して返す必要があります。 アクティビティ フィード XML の例については、「アクティビティ フィード [XML の例」を参照してください](activity-feed-xml-example.md)。 友人のアクティビティの同期の詳細については、「友人とアクティビティの同期 [」を参照してください](synchronizing-friends-and-activities.md)。 OSC プロバイダー XML スキーマの完全な定義 (必須または省略可能な要素を含む) については、「ソーシャル コネクタ プロバイダー XML スキーマOutlook[を参照してください](outlook-social-connector-provider-xml-schema.md)。 
  
次のシナリオでは、OSC は People Pane で選択されたユーザーのアクティビティを動的に同期し、そのユーザーの詳細を取得します。
  
1. アクティビティのオンデマンド同期をサポートする OSC プロバイダーは **、getActivities** 要素と **dynamicActivitiesLookupEx** 要素を使用して OSC に対してそれを示します。 OSC プロバイダーは **、hashFunction 要素も設定** します。 3 つの要素はすべて、機能の子 **要素です**。 
    
2. OSC プロバイダーは **、ISocialProvider::GetCapabilities** および [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) メソッドを実装します。 
    
3. OSC は **ISocialProvider::GetCapabilities** を呼び出して **、getActivities** と **dynamicActivitiesLookupEx** の値をチェックして、OSC プロバイダーがアクティビティのオンデマンド同期をサポートしているか確認します。 OSC は、OSC プロバイダーがサポートする **hashFunction** 要素の値もメモします。 
    
4. OSC は、ユーザー ウィンドウまたは連絡先カードを更新して、選択したユーザーの最新のアクティビティをユーザーに表示します。 OSC は **、hashFunction** 要素で指定されたハッシュ関数を使用して、そのユーザーの SMTP アドレスを暗号化し **、hashedAddresses** 要素の XML スキーマ定義に準拠する XML 文字列を形成します。 
    
5. OSC は **ISocialSession2::GetActivitiesEx** を呼び出し、ハッシュされたアドレスのこの XML 文字列を  _hashedAddresses_ パラメーターとして提供し  _、activities_ パラメーター内のそのユーザーのアクティビティの現在のコレクションを取得します。 activity  _パラメーター_ 文字列は、activityFeed 要素の XML スキーマ定義 **に準拠** しています。 
    
6. **activityFeed** の XML スキーマ定義に基づいて、OSC はアクティビティ文字列をさらに解析して、各アクティビティの種類、発行日、その他の情報、およびアクティビティの表示方法を確認します。 
    
7. 選択した人物の詳細を取得するために、OSC は [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md)を呼び出し  _、personsAddresses_ パラメーターの引数と同じ XML 文字列のハッシュアドレスを提供します。 ユーザーに関する詳細は  _、personsCollection パラメーターで返_ されます。 これらの詳細には **、firstName、lastName、emailAddress****を含めできます**。  _personsCollection パラメーター_ は、person 要素の XML スキーマ定義に **準拠** しています。 
    
アクティビティの XML の指定の詳細については、このセクションの次のトピックを参照してください。
  
- [アクティビティ フィード アイテムの XML の概要](overview-of-xml-for-an-activity-feed-item.md)
    
- [activityDetails 要素](activitydetails-element.md)
    
- [activityTemplateContainer 要素](activitytemplatecontainer-element.md)
    
- [テンプレート変数](template-variables.md)
    
- [アクティビティを適切に表示するためのガイドライン](guidelines-for-properly-displaying-activities.md)
    
## <a name="see-also"></a>関連項目

- [アクティビティ フィード XML の例](activity-feed-xml-example.md)  
- [フレンドとアクティビティの同期](synchronizing-friends-and-activities.md) 
- [機能の XML](xml-for-capabilities.md)  
- [友人のための XML](xml-for-friends.md)
- [OSC XML スキーマを使用したプロバイダーの開発](developing-a-provider-with-the-osc-xml-schema.md)

