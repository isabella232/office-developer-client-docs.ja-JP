---
title: アクティビティの取得
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 8cb8f916-f061-4c4c-ad1b-40d44af3345a
description: OSC は ISocialProvider::GetCapabilities メソッドを呼び出して、ソーシャル ネットワークの OSC プロバイダーの機能を決定します。
ms.openlocfilehash: c1d34913a372c3959b34322eadf9964dcbbeb054
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590458"
---
# <a name="getting-activities"></a>アクティビティの取得

OSC は [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) メソッドを呼び出して、ソーシャル ネットワークの OSC プロバイダーの機能を決定します。 返される機能 XML の **getActivities** 要素と **dynamicActivitiesLookupEx** 要素 **が、OSC** プロバイダーがオンデマンドでアクティビティを取得し、アクティビティをメモリに格納するサポートを示している場合、OSC は次の呼び出しシーケンスを実行できます。 OSC は、機能 XML の **hashFunction** 要素で指定されたハッシュ **関数もメモします** 。 OSC は、次の順序でメソッドを呼び出して、ソーシャル ネットワーク上の友人や友人以外のアクティビティと情報を取得します [(ISocialPerson](isocialpersoniunknown.md) インターフェイスでサポートされています)。 
  
1. [ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) —認証プロセスの最後に、OSC は **GetLoggedOnUser** を呼び出して、認証されるユーザーの [ISocialProfile](isocialprofileisocialperson.md) インターフェイスを取得します。 認証の詳細については [、「Basic Authentication and](basic-authentication.md) [Forms-Based Authentication」を参照してください](forms-based-authentication.md)。
    
2. [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) —Outlook People Pane に表示されるユーザーの場合、OSC は SMTP アドレスを取得してハッシュし **、ISocialSession2::GetActivitiesEx** を呼び出し、これらのユーザーに対して返されるアクティビティ データを (メモリ内に) 格納します。 OSC は、ログオンしているユーザーの友人のアクティビティのコレクションを含む文字列である出力パラメーター activities を取得します。 この文字列は **、activityFeed** 要素のスキーマ定義に準拠しています。 
    
3. [ISocialSession::GetPerson](isocialsession-getperson.md) **—GetActivitiesEx** によって返される **activityFeed** XML の **activityDetails** 要素ごとに、そのアクティビティを所有するユーザーを示す **ownerID** 要素があります。 OSC は、 **その ownerID 値** を使用して **GetPerson** を呼び出して、そのユーザー **の ISocialPerson** インターフェイスを取得します。 
    
4. [ISocialPerson::GetDetails](isocialperson-getdetails.md) —手順 3 から取得した **ISocialPerson** オブジェクトに基づいて、OSC は **GetDetails** を呼び出して、名や名など、その人物の詳細を取得します。 OSC は、手順 2 の **GetActivitiesEx** によって返される **activityFeed** XML の **activityDetails** 要素で指定されたアクティビティごとに同じ操作を実行できます。 
    
> [!NOTE]
> OSC は、既定の間隔でアクティビティ キャッシュを更新します。 アクティビティ キャッシュの更新の詳細については、「友人とアクティビティの [同期」を参照してください](synchronizing-friends-and-activities.md)。 
  
## <a name="see-also"></a>関連項目

- [機能の XML](xml-for-capabilities.md)
- [OSC の一般的な呼び出しシーケンス](osc-typical-calling-sequences.md)

