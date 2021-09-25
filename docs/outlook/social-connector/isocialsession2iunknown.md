---
title: ISocialSession2 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f516e86e-0158-472b-9711-fe7491b24404
description: キャッシュされた資格情報を使用して、フレンドの追加、フレンドのオンデマンドまたはハイブリッド同期、アクティビティのオンデマンド同期、またはソーシャル ネットワークへのログオンをサポートします。
ms.openlocfilehash: 4c6b34b01092c215cca5c18d332c3ec6e28647fd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574504"
---
# <a name="isocialsession2--iunknown"></a>ISocialSession2 : IUnknown

キャッシュされた資格情報を使用して、フレンドの追加、フレンドのオンデマンドまたはハイブリッド同期、アクティビティのオンデマンド同期、またはソーシャル ネットワークへのログオンをサポートします。
  
## <a name="members"></a>メンバー

次の表に **、ISocialSession2** インターフェイスで使用できるメンバーを示します。 
  
|**名前**|**メンバーの種類**|**説明**|
|:-----|:-----|:-----|
|[FollowPersonEx](isocialsession2-followpersonex.md) <br/> |Method  <br/> |_emailAddresses_ パラメーターと _displayName_ パラメーターで識別されるユーザーを、ソーシャル ネットワーク上のログオンユーザーのフレンドとして追加します。  <br/> |
|[GetActivitiesEx](isocialsession2-getactivitiesex.md) <br/> |Method  <br/> |_hashedAddresses_ パラメーターで指定されたユーザーのアクティビティのコレクションを表す文字列を取得します。  <br/> |
|[GetPeopleDetails](isocialsession2-getpeopledetails.md) <br/> |Method  <br/> |_personsAddresses_ パラメーターで指定されたユーザーの人物と画像の詳細のコレクションを含む文字列を返します。  <br/> |
|[LogonCached](isocialsession2-logoncached.md) <br/> |Method  <br/> |キャッシュされた資格情報を使用してソーシャル ネットワーク サイトにログオンします。  <br/> |
   
## <a name="remarks"></a>注釈

Outlook ソーシャル コネクタ (OSC) プロバイダーは、プロバイダーが友人のオンデマンドまたはハイブリッド同期、アクティビティのオンデマンド同期、キャッシュされた資格情報を使用してソーシャル ネットワークにログオンする場合に、このインターフェイスを実装できます。 OSC プロバイダーが **ISocialSession2** を実装し、ソーシャル ネットワーク上で次のユーザーをサポートしている場合、OSC は [ISocialSession::FollowPerson](isocialsession-followperson.md)の代わりに [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md)を呼び出し、プロバイダーは **ISocialSession2::FollowPersonEx** も実装する必要があります。
  
## <a name="see-also"></a>関連項目

- [Outlookソーシャル コネクタ プロバイダー インターフェイス](outlook-social-connector-provider-interfaces.md)

