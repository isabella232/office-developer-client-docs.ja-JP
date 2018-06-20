---
title: 活動を取得します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cb8f916-f061-4c4c-ad1b-40d44af3345a
description: OSC では、ソーシャル ネットワークの OSC プロバイダーの機能を決定する ISocialProvider::GetCapabilities メソッドを呼び出します。
ms.openlocfilehash: 82bb5322118fa3ebd7610f56b8f34ae95b59a40f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804332"
---
# <a name="getting-activities"></a>活動を取得します。

OSC では、ソーシャル ネットワークの OSC プロバイダーの機能を決定する[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)メソッドを呼び出します。 **GetActivities**と**dynamicActivitiesLookupEx** **機能**の返された XML 要素では、OSC プロバイダーが要求と活動をメモリに格納することで取得の活動をサポートしていることを示す、OSC、次のことができます。呼び出しシーケンスです。 OSC では、ハッシュ関数を**実装しています。** 要素で XML の**機能**を指定もメモします。 OSC では、活動と情報を取得 ( [ISocialPerson](isocialpersoniunknown.md)インターフェイスでサポートされている)、ソーシャル ネットワーク上の非友人や友人を次の順序でメソッドを呼び出します。 
  
1. [ISocialSession::GetLoggedOnUser](isocialsession-getloggedonuser.md) -、OSC は認証プロセスの最後に、ユーザーが認証されるための[ISocialProfile](isocialprofileisocialperson.md)インターフェイスを取得するのには**GetLoggedOnUser**を呼び出します。 認証の詳細については、[基本認証](basic-authentication.md)と[フォーム ベース認証](forms-based-authentication.md)を参照してください。
    
2. [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) -、OSC を取得 Outlook 人物情報ウィンドウに表示されている担当者、およびに返されたハッシュの SMTP アドレスを**ISocialSession2::GetActivitiesEx**を呼び出して、(メモリ内) のアクティビティ データを格納します。これらの担当者。 OSC は、_アクティビティ_、ログオン中のユーザーの友人の活動のコレクションを格納する文字列には、出力パラメーターを取得します。 この文字列は、 **activityFeed**要素のスキーマ定義に準拠しています。 
    
3. [ISocialSession::GetPerson](isocialsession-getperson.md) - **activityFeed** **GetActivitiesEx**から返された XML 内の**activityDetails**要素ごとには、その活動を所有する人物の**ownerID**要素です。 OSC では、その**ownerID**値を使用して、その人の**ISocialPerson**インターフェイスを取得するのには**GetPerson**を呼び出します。 
    
4. [ISocialPerson::GetDetails](isocialperson-getdetails.md) -、OSC 3 のステップから取得された**ISocialPerson**オブジェクトに基づき、名、姓、名など、その人の詳細を取得する**GetDetails**を呼び出します。 OSC **activityFeed**手順 2 で、 **GetActivitiesEx**から返された XML 内の**activityDetails**要素で指定されているそれぞれのアクティビティで同じことが行えます。 
    
> [!NOTE]
> OSC では、既定の間隔で活動のキャッシュを更新します。 活動キャッシュの更新の詳細については、[同期の友人との活動](synchronizing-friends-and-activities.md)を参照してください。 
  
## <a name="see-also"></a>関連項目

- [機能のための XML](xml-for-capabilities.md)
- [OSC の典型的な呼び出しシーケンス](osc-typical-calling-sequences.md)

