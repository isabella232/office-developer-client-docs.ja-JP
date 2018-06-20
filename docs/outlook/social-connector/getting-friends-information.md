---
title: フレンド情報の取得
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d8a56746-4de4-4f24-af32-e85079c060b8
description: Outlook ソーシャル コネクタ (OSC) では、ソーシャル ネットワークの OSC プロバイダーの機能を決定する ISocialProvider::GetCapabilities メソッドを呼び出します。
ms.openlocfilehash: 68443992351f4c83e8e560a753941e97bf91de67
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804329"
---
# <a name="getting-friends-information"></a>フレンド情報の取得

Outlook ソーシャル コネクタ (OSC) では、ソーシャル ネットワークの OSC プロバイダーの機能を決定する[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)メソッドを呼び出します。 **機能**の返された XML 内の**getFriends**と**cacheFriends**の要素を示す OSC プロバイダーには、取得の友人がサポートしていることと、対応する連絡先フォルダー内のアイテムが Outlook とキャッシュの友人にお問い合わせください、OSC のことができます。次の呼び出しシーケンスです。 OSC では、取得する情報と画像 ( [ISocialPerson](isocialpersoniunknown.md)インターフェイスでサポートされている)、ソーシャル ネットワーク上の友人のこの順序でメソッドを呼び出します。 
  
> [!NOTE]
> OSC では、既定の間隔でキャッシュを更新します。 キャッシュ中にエラーが発生した場合を更新する XML の**機能**に**contactSyncRestartInterval**要素を指定することによって制御することも別のプリセットの間隔で OSC 再試行します。 連絡先のキャッシュの更新の詳細については、[同期の友人との活動](synchronizing-friends-and-activities.md)を参照してください。 
  
1. [ISocialSession::LoggedOnUserID](isocialsession-loggedonuserid.md) -「OSC は、ソーシャル ネットワークにログオンしている Office ユーザーのユーザー ID を取得します。 
    
2. [ISocialSession::GetPerson](isocialsession-getperson.md) -Office ユーザーのユーザー ID を使用すると、OSC **ISocialPerson**のオブジェクトを取得するユーザーです。 
    
3. [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) -「OSC は、ソーシャル ネットワークのユーザーのフレンド リストを取得します。 
    
4. [ISocialSession::GetPerson](isocialsession-getperson.md) : XML の各メンバーは、 **GetFriendsAndColleagues**によって返される、ため、OSC は**ISocialPerson**インターフェイスを取得します。 
    
5. [ISocialPerson::GetPicture](isocialperson-getpicture.md) -、OSC が画像リソースを取得する XML の各メンバーは、 **GetFriendsAndColleagues**によって返される、ためです。
    
## <a name="see-also"></a>関連項目

- [機能のための XML](xml-for-capabilities.md)
- [OSC の典型的な呼び出しシーケンス](osc-typical-calling-sequences.md)

