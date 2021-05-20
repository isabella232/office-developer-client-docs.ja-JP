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
ms.openlocfilehash: c60fab1c27d2f761db28ed06bb45080857630e8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437827"
---
# <a name="isocialsession--iunknown"></a>ISocialSession : IUnknown

ソーシャル ネットワーク サイトへの接続を表します。
  
## <a name="members"></a>Members

次の表に **、ISocialSession** インターフェイスで使用できるメンバーを示します。 
  
|**名前**|**メンバーの種類**|**説明**|
|:-----|:-----|:-----|
|[FindPerson](isocialsession-findperson.md) <br/> |メソッド  <br/> |userID パラメーターに一致する 1 人または複数のユーザーを表す  _文字列を取得_ します。  <br/> |
|[FollowPerson](isocialsession-followperson.md) <br/> |メソッド  <br/> |_emailAddress_ パラメーターで識別されたユーザーを、ソーシャル ネットワーク上のログオンユーザーのフレンドとして追加します。  <br/> |
|[GetActivities](isocialsession-getactivities.md) <br/> |メソッド  <br/> |このメソッドは、ソーシャル Outlook (OSC) 1.1 で廃止されました。  <br/> |
|[GetLoggedOnUser](isocialsession-getloggedonuser.md) <br/> |メソッド  <br/> |ログオンしている [ユーザーを表す ISocialProfile](isocialprofileisocialperson.md) インターフェイスを取得します。  <br/> |
|[GetLogonUrl](isocialsession-getlogonurl.md) <br/> |メソッド  <br/> |Web 認証中にブラウザー ベースのフォームをユーザーに表示するために使用される URL を表す文字列を取得します。  <br/> |
|[GetNetworkIdentifier](isocialsession-getnetworkidentifier.md) <br/> |メソッド  <br/> |特定のソーシャル ネットワーク接続の一意のソーシャル ネットワーク識別子を表す文字列を取得します。  <br/> |
|[GetPerson](isocialsession-getperson.md) <br/> |メソッド  <br/> |userID [パラメーターに基づいて ISocialPerson](isocialpersoniunknown.md) インターフェイス  _を取得_ します。  <br/> |
|[LoggedOnUserID](isocialsession-loggedonuserid.md) <br/> |プロパティ  <br/> |現在ログオンしているユーザーのソーシャル ネットワーク ユーザー ID を表す文字列を返します。  <br/> |
|[LoggedOnUserName](isocialsession-loggedonusername.md) <br/> |プロパティ  <br/> |ログオン時に使用されるユーザー名を表す文字列を返します。  <br/> |
|[Logon](isocialsession-logon.md) <br/> |メソッド  <br/> |指定したユーザー名とパスワードを使用してソーシャル ネットワーク サイトにログオンします。  <br/> |
|[LogonWeb](isocialsession-logonweb.md) <br/> |メソッド  <br/> |フォーム ベース認証を使用してソーシャル ネットワーク サイトにログオンします。  <br/> |
|[SiteUrl](isocialsession-siteurl.md) <br/> |プロパティ  <br/> |ソーシャル ネットワーク サイトの URL を設定します。  <br/> |
|[UnFollowPerson](isocialsession-unfollowperson.md) <br/> |メソッド  <br/> |ソーシャル ネットワーク上のフレンドとして  _userID_ パラメーターによって識別されたユーザーを削除します。  <br/> |
   
## <a name="remarks"></a>注釈

OSC プロバイダーは、OSC と通信するためにこのインターフェイスを実装する必要があります。
  
## <a name="see-also"></a>関連項目

- [Outlookソーシャル コネクタ プロバイダー インターフェイス](outlook-social-connector-provider-interfaces.md)

