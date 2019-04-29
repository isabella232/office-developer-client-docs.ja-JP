---
title: 友だち情報の取得
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d8a56746-4de4-4f24-af32-e85079c060b8
description: 'Outlook social Connector (.osc) は、imethod alprovider:: getcapabilities メソッドを呼び出して、ソーシャルネットワークの .osc プロバイダーの機能を判別します。'
ms.openlocfilehash: 697902631b010afab015e9cfb73fac81ac427d6e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428796"
---
# <a name="getting-friends-information"></a>友だち情報の取得

Outlook social Connector (.osc) は、 [imethod alprovider:: getcapabilities](isocialprovider-getcapabilities.md)メソッドを呼び出して、ソーシャルネットワークの .osc プロバイダーの機能を判別します。 返された**機能**XML の**getfriends**要素と**cacheFriends**要素が、.osc プロバイダーが、対応する連絡先フォルダーにある Outlook の連絡先アイテムとしてフレンドをキャッシュすることをサポートしていることを示している場合は、.osc次の呼び出しシーケンス。 .osc は、このシーケンスのメソッドを呼び出して、ソーシャルネットワーク上のフレンドの情報と画像 ( [isocial alperson](isocialpersoniunknown.md)インターフェイスでサポートされる) を取得します。 
  
> [!NOTE]
> .osc は、既定の間隔でキャッシュを更新します。 キャッシュ更新中にエラーが発生した場合、.osc は別の事前設定された間隔で再試行を行います。これは、 **capabilities** XML の**contactsyncrestartinterval**要素を指定することによって制御することもできます。 連絡先キャッシュの更新の詳細については、「[友人とアクティビティを同期](synchronizing-friends-and-activities.md)する」を参照してください。 
  
1. [iLoggedOnUserID alsession::](isocialsession-loggedonuserid.md) — .osc は、ソーシャルネットワークにログオンしている Office ユーザーのユーザー ID を取得します。 
    
2. i入力された[セッション:: getperson](isocialsession-getperson.md) -Office ユーザーのユーザー ID を使用して、.osc はそのユーザーの**isocialsession**オブジェクトを取得します。 
    
3. [iGetFriendsAndColleagues:](isocialperson-getfriendsandcolleagues.md) .osc は、ソーシャルネットワーク上のユーザーのフレンドリストを取得します。 
    
4. [iGetFriendsAndColleagues alsession:: getperson](isocialsession-getperson.md) — **** によって返される XML 内の各ユーザーについて、.osc は**i alperson**インターフェイスを取得します。 
    
5. [ichanged alperson:: getpicture](isocialperson-getpicture.md) — **GetFriendsAndColleagues**によって返される XML 内の各ユーザーについて、.osc が画像リソースを取得します。
    
## <a name="see-also"></a>関連項目

- [機能の XML](xml-for-capabilities.md)
- [通常の呼び出しシーケンスの .osc](osc-typical-calling-sequences.md)

