---
title: アクティビティの取得
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cb8f916-f061-4c4c-ad1b-40d44af3345a
description: '.osc は、ソーシャルネットワークの .osc プロバイダーの機能を判断するために、imethod alprovider:: getcapabilities メソッドを呼び出します。'
ms.openlocfilehash: 9d504fb64368a6910feaa38f0ef19ed631b4d4e3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327189"
---
# <a name="getting-activities"></a>アクティビティの取得

.osc は、ソーシャルネットワークの .osc プロバイダーの機能を判断するために、 [imethod alprovider:: getcapabilities](isocialprovider-getcapabilities.md)メソッドを呼び出します。 返された**機能**XML の**getactivities**要素と**dynamicActivitiesLookupEx**要素が、.osc プロバイダーが必要に応じてアクティビティを取得し、アクティビティをメモリに格納していることを示している場合、.osc は次のことを行うことができます。呼び出しシーケンス。 また、.osc は、 **capabilities** XML の**hashfunction**要素で指定されているハッシュ関数についても注意してください。 .osc は、ソーシャルネットワーク上の友人および友人以外のアクティビティと情報 (isocial [alperson](isocialpersoniunknown.md)インターフェイスでサポートされる) を取得するために、次のシーケンスのメソッドを呼び出します。 
  
1. [iGetLoggedOnUser alsession::](isocialsession-getloggedonuser.md) —認証プロセスの最後に、.osc が**GetLoggedOnUser**を呼び出して、認証されているユーザーの[i alprofile](isocialprofileisocialperson.md)インターフェイスを取得します。 認証の詳細については、「[基本認証](basic-authentication.md)」および「[フォームベース認証](forms-based-authentication.md)」を参照してください。
    
2. [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md) — [Outlook People] ウィンドウに表示されている人の場合、このアクティビティは SMTP アドレスを取得してハッシュし、 **ISocialSession2::::: GetActivitiesEx**、およびストア (メモリ) を呼び出します。返されるアクティビティデータこれらの人物。 .osc は、出力パラメーター [_アクティビティ_] を取得します。これは、ログオンしているユーザーのフレンドのアクティビティのコレクションを含む文字列です。 この文字列は、 **activityfeed**要素のスキーマ定義に準拠しています。 
    
3. [iGetActivitiesEx alsession:: getperson](isocialsession-getperson.md) — **** によって返される**activitydetails** XML 内の各**activitydetails**要素に、そのアクティビティを所有しているユーザーを示す**ownerID**要素があります。 .osc は、その**ownerID**値を使用して**getperson**を呼び出し、その人物の**i alperson**インターフェイスを取得します。 
    
4. [ichanged alperson:: getdetails](isocialperson-getdetails.md) —手順3で取得した**i指定 alperson**オブジェクトに基づき、.osc は**getdetails**を呼び出して、その人物 (名や姓など) の詳細を取得します。 この .osc は、手順2で**GetActivitiesEx**によって返される**activitydetails** XML の**activitydetails**要素で指定されている各アクティビティに対して同じ操作を行うことができます。 
    
> [!NOTE]
> .osc は、アクティビティキャッシュを既定の間隔で更新します。 アクティビティキャッシュの更新の詳細については、「[友人とアクティビティを同期](synchronizing-friends-and-activities.md)する」を参照してください。 
  
## <a name="see-also"></a>関連項目

- [機能の XML](xml-for-capabilities.md)
- [通常の呼び出しシーケンスの .osc](osc-typical-calling-sequences.md)

