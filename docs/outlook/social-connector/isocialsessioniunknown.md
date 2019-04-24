---
title: i、alsession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0fe423d7-b044-479b-89ad-c39620eedd65
description: ソーシャルネットワークサイトへの接続を表します。
ms.openlocfilehash: c60fab1c27d2f761db28ed06bb45080857630e8d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357366"
---
# <a name="isocialsession--iunknown"></a>ISocialSession : IUnknown

ソーシャルネットワークサイトへの接続を表します。
  
## <a name="members"></a>Members

次の表に、 **iare alsession**インターフェイスで使用できるメンバーを示します。 
  
|**Name**|**メンバーの種類**|**説明**|
|:-----|:-----|:-----|
|[findperson](isocialsession-findperson.md) <br/> |メソッド  <br/> |_userID_パラメーターに一致する1人以上の人物を表す文字列を取得します。  <br/> |
|[ユーザー](isocialsession-followperson.md) <br/> |メソッド  <br/> |ソーシャルネットワークにログオンしているユーザーのフレンドとして、 _emailAddress_パラメーターによって識別された人物を追加します。  <br/> |
|[getactivities](isocialsession-getactivities.md) <br/> |メソッド  <br/> |このメソッドは、Outlook Social Connector (.osc) 1.1 で廃止されました。  <br/> |
|[GetLoggedOnUser](isocialsession-getloggedonuser.md) <br/> |メソッド  <br/> |ログオンユーザーを表す[isocialprofile](isocialprofileisocialperson.md)インターフェイスを取得します。  <br/> |
|[getlogonurl](isocialsession-getlogonurl.md) <br/> |メソッド  <br/> |web 認証中にブラウザーベースのフォームをユーザーに提示するために使用される URL を表す文字列を取得します。  <br/> |
|[getnetworkidentifier](isocialsession-getnetworkidentifier.md) <br/> |メソッド  <br/> |特定のソーシャルネットワーク接続の一意のソーシャルネットワーク識別子を表す文字列を取得します。  <br/> |
|[getperson](isocialsession-getperson.md) <br/> |メソッド  <br/> |_userID_パラメーターに基づいて[isocialperson](isocialpersoniunknown.md)インターフェイスを取得します。  <br/> |
|[LoggedOnUserID](isocialsession-loggedonuserid.md) <br/> |プロパティ  <br/> |現在ログオンしているユーザーのソーシャルネットワークユーザー ID を表す文字列を返します。  <br/> |
|[LoggedOnUserName](isocialsession-loggedonusername.md) <br/> |プロパティ  <br/> |ログオン時に使用されるユーザー名を表す文字列を返します。  <br/> |
|[Logon](isocialsession-logon.md) <br/> |メソッド  <br/> |指定したユーザー名とパスワードを使用して、ソーシャルネットワークサイトにログオンします。  <br/> |
|[logonweb](isocialsession-logonweb.md) <br/> |メソッド  <br/> |フォームベース認証を使用してソーシャルネットワークサイトにログオンします。  <br/> |
|[SiteUrl](isocialsession-siteurl.md) <br/> |プロパティ  <br/> |ソーシャルネットワークサイトの URL を設定します。  <br/> |
|[個人](isocialsession-unfollowperson.md) <br/> |メソッド  <br/> |_userID_パラメーターで指定された人物をソーシャルネットワーク上のフレンドとして削除します。  <br/> |
   
## <a name="remarks"></a>解説

.osc プロバイダーは、このインターフェイスを実装して、.osc と通信する必要があります。
  
## <a name="see-also"></a>関連項目

- [Outlook Social Connector プロバイダーインターフェイス](outlook-social-connector-provider-interfaces.md)

