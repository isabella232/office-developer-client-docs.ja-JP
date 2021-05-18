---
title: ISocialSession2 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f516e86e-0158-472b-9711-fe7491b24404
description: キャッシュされた資格情報を使用して、フレンドの追加、フレンドのオンデマンドまたはハイブリッド同期、アクティビティのオンデマンド同期、またはソーシャル ネットワークへのログオンをサポートします。
ms.openlocfilehash: 6dc581bb812408d7e01f94c375671783445616a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408832"
---
# <a name="isocialsession2--iunknown"></a>ISocialSession2 : IUnknown

キャッシュされた資格情報を使用して、フレンドの追加、フレンドのオンデマンドまたはハイブリッド同期、アクティビティのオンデマンド同期、またはソーシャル ネットワークへのログオンをサポートします。
  
## <a name="members"></a>Members

次の表に **、ISocialSession2** インターフェイスで使用できるメンバーを示します。 
  
|**名前**|**メンバーの種類**|**説明**|
|:-----|:-----|:-----|
|[FollowPersonEx](isocialsession2-followpersonex.md) <br/> |メソッド  <br/> |_emailAddresses_ パラメーターと _displayName_ パラメーターで識別されるユーザーを、ソーシャル ネットワーク上のログオンユーザーのフレンドとして追加します。  <br/> |
|[GetActivitiesEx](isocialsession2-getactivitiesex.md) <br/> |メソッド  <br/> |_hashedAddresses_ パラメーターで指定されたユーザーのアクティビティのコレクションを表す文字列を取得します。  <br/> |
|[GetPeopleDetails](isocialsession2-getpeopledetails.md) <br/> |メソッド  <br/> |_personsAddresses_ パラメーターで指定されたユーザーの人物と画像の詳細のコレクションを含む文字列を返します。  <br/> |
|[LogonCached](isocialsession2-logoncached.md) <br/> |メソッド  <br/> |キャッシュされた資格情報を使用してソーシャル ネットワーク サイトにログオンします。  <br/> |
   
## <a name="remarks"></a>注釈

Outlook ソーシャル コネクタ (OSC) プロバイダーは、プロバイダーが友人のオンデマンドまたはハイブリッド同期、アクティビティのオンデマンド同期、キャッシュされた資格情報を使用してソーシャル ネットワークにログオンする場合に、このインターフェイスを実装できます。 OSC プロバイダーが **ISocialSession2** を実装し、ソーシャル ネットワーク上で次のユーザーをサポートしている場合、OSC は [ISocialSession::FollowPerson](isocialsession-followperson.md)の代わりに [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md)を呼び出し、プロバイダーは **ISocialSession2::FollowPersonEx** も実装する必要があります。
  
## <a name="see-also"></a>関連項目

- [Outlookソーシャル コネクタ プロバイダー インターフェイス](outlook-social-connector-provider-interfaces.md)

