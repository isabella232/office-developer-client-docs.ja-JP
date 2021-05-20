---
title: 友だち情報の取得
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d8a56746-4de4-4f24-af32-e85079c060b8
description: ソーシャル Outlook (OSC) は、ISocialProvider::GetCapabilities メソッドを呼び出して、ソーシャル ネットワークの OSC プロバイダーの機能を決定します。
ms.openlocfilehash: 697902631b010afab015e9cfb73fac81ac427d6e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428796"
---
# <a name="getting-friends-information"></a>友だち情報の取得

ソーシャル Outlook (OSC) は[、ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)メソッドを呼び出して、ソーシャル ネットワークの OSC プロバイダーの機能を決定します。 返される機能 **XML** の **getFriends** 要素と **cacheFriends** 要素が、OSC プロバイダーが対応する連絡先フォルダー内の Outlook 連絡先アイテムとしてフレンドの取得と友人のキャッシュをサポートしている場合、OSC は次の呼び出しシーケンスを実行できます。 OSC は、このシーケンス内のメソッドを呼び出して、ソーシャル ネットワーク上のフレンドの情報と画像 [(ISocialPerson](isocialpersoniunknown.md) インターフェイスでサポートされている) を取得します。 
  
> [!NOTE]
> OSC は、既定の間隔でキャッシュを更新します。 キャッシュ更新中にエラーが発生した場合、OSC は別の事前設定された間隔で再試行します。また、機能 **XML** で **contactSyncRestartInterval** 要素を指定することで制御することもできます。 連絡先キャッシュの更新の詳細については、「友人とアクティビティの [同期」を参照してください](synchronizing-friends-and-activities.md)。 
  
1. [ISocialSession::LoggedOnUserID](isocialsession-loggedonuserid.md) —OSC は、ソーシャル ネットワークにログオンしている Office ユーザーのユーザー ID を取得します。 
    
2. [ISocialSession::GetPerson](isocialsession-getperson.md) —Office ユーザーのユーザー ID を使用して、OSC は、そのユーザーの **ISocialPerson** オブジェクトを取得します。 
    
3. [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) —OSC は、ソーシャル ネットワーク上でユーザーのフレンド リストを取得します。 
    
4. [ISocialSession::GetPerson](isocialsession-getperson.md) **—GetFriendsAndColleagues** によって返される XML 内の各ユーザーについて、OSC は **ISocialPerson** インターフェイスを取得します。 
    
5. [ISocialPerson::GetPicture](isocialperson-getpicture.md) **—GetFriendsAndColleagues** によって返される XML 内の各ユーザーについて、OSC はピクチャ リソースを取得します。
    
## <a name="see-also"></a>関連項目

- [機能の XML](xml-for-capabilities.md)
- [OSC の一般的な呼び出しシーケンス](osc-typical-calling-sequences.md)

