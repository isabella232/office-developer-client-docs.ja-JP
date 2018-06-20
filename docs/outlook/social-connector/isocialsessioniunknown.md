---
title: ISocialSession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0fe423d7-b044-479b-89ad-c39620eedd65
description: ソーシャル ネットワーク サイトへの接続を表します。
ms.openlocfilehash: ee3a8aa72ea187b4c211bc7a49e8a2dbe170adad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804381"
---
# <a name="isocialsession--iunknown"></a>ISocialSession: IUnknown

ソーシャル ネットワーク サイトへの接続を表します。
  
## <a name="members"></a>メンバー

次の表は、 **ISocialSession**インターフェイスで使用可能なメンバーを示します。 
  
|**名前**|**メンバーの種類**|**説明**|
|:-----|:-----|:-----|
|[FindPerson](isocialsession-findperson.md) <br/> |メソッド  <br/> |_ユーザー Id_パラメーターに一致する 1 つまたは複数の人物を表す文字列を取得します。  <br/> |
|[FollowPerson](isocialsession-followperson.md) <br/> |メソッド  <br/> |ソーシャル ネットワークにログオン中のユーザーのフレンドとして、 _emailAddress_パラメーターで識別されるユーザーを追加します。  <br/> |
|[GetActivities](isocialsession-getactivities.md) <br/> |メソッド  <br/> |この方法で Outlook ソーシャル コネクタ (OSC) 1.1 は廃止されました。  <br/> |
|[GetLoggedOnUser](isocialsession-getloggedonuser.md) <br/> |メソッド  <br/> |ログオン中のユーザーを表す[ISocialProfile](isocialprofileisocialperson.md)インターフェイスを取得します。  <br/> |
|[GetLogonUrl](isocialsession-getlogonurl.md) <br/> |メソッド  <br/> |Web 認証時にユーザーにブラウザー ベースのフォームを表示するために使用される URL を表す文字列を取得します。  <br/> |
|[GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) <br/> |メソッド  <br/> |特定のソーシャル ネットワークの接続のソーシャル ネットワークの一意の識別子を表す文字列を取得します。  <br/> |
|[GetPerson](isocialsession-getperson.md) <br/> |メソッド  <br/> |_ユーザー Id_のパラメーターに基づいて、 [ISocialPerson](isocialpersoniunknown.md)インターフェイスを取得します。  <br/> |
|[LoggedOnUserID](isocialsession-loggedonuserid.md) <br/> |Property  <br/> |現在ログオンしているユーザーのソーシャル ネットワークのユーザー ID を表す文字列を返します。  <br/> |
|[LoggedOnUserName](isocialsession-loggedonusername.md) <br/> |Property  <br/> |ログオン時に使用されるユーザー名を表す文字列を返します。  <br/> |
|[Logon](isocialsession-logon.md) <br/> |メソッド  <br/> |指定されたユーザー名とパスワードを使用して、ソーシャル ネットワーク サイトにログオンします。  <br/> |
|[LogonWeb](isocialsession-logonweb.md) <br/> |メソッド  <br/> |フォーム ベース認証を使用して、ソーシャル ネットワーク サイトにログオンします。  <br/> |
|[SiteUrl](isocialsession-siteurl.md) <br/> |Property  <br/> |ソーシャル ネットワーク サイトの URL を設定します。  <br/> |
|[UnFollowPerson](isocialsession-unfollowperson.md) <br/> |メソッド  <br/> |ソーシャル ネットワークの友人として、_ユーザー Id_のパラメーターで識別されるユーザーを削除します。  <br/> |
   
## <a name="remarks"></a>備考

OSC プロバイダーでは、OSC と通信するには、このインターフェイスを実装する必要があります。
  
## <a name="see-also"></a>関連項目

- [Outlook ソーシャル コネクタ プロバイダー インターフェイス](outlook-social-connector-provider-interfaces.md)

