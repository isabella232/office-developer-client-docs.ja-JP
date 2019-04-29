---
title: ISocialSession2 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f516e86e-0158-472b-9711-fe7491b24404
description: フレンドのフレンド、オンデマンドまたはハイブリッド同期の追加、アクティビティのオンデマンド同期、またはキャッシュされた資格情報を使用したソーシャルネットワークへのログオンをサポートしています。
ms.openlocfilehash: 6dc581bb812408d7e01f94c375671783445616a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408832"
---
# <a name="isocialsession2--iunknown"></a>ISocialSession2 : IUnknown

フレンドのフレンド、オンデマンドまたはハイブリッド同期の追加、アクティビティのオンデマンド同期、またはキャッシュされた資格情報を使用したソーシャルネットワークへのログオンをサポートしています。
  
## <a name="members"></a>メンバー

次の表に、 **ISocialSession2**インターフェイスで使用できるメンバーを示します。 
  
|**名前**|**メンバーの種類**|**説明**|
|:-----|:-----|:-----|
|[この例](isocialsession2-followpersonex.md) <br/> |メソッド  <br/> |_emailaddresses_および_displayName_パラメーターで指定された人物を、ソーシャルネットワーク上のログオンユーザーのフレンドとして追加します。  <br/> |
|[GetActivitiesEx](isocialsession2-getactivitiesex.md) <br/> |メソッド  <br/> |_hashedAddresses_パラメーターによって指定されたユーザーのアクティビティのコレクションを表す文字列を取得します。  <br/> |
|[GetPeopleDetails](isocialsession2-getpeopledetails.md) <br/> |メソッド  <br/> |ユーザーの個人情報および画像の詳細のコレクションが含まれている文字列を返し__ ます。  <br/> |
|[logoncached](isocialsession2-logoncached.md) <br/> |メソッド  <br/> |キャッシュされた資格情報を使用してソーシャルネットワークサイトにログオンします。  <br/> |
   
## <a name="remarks"></a>注釈

Outlook Social Connector (.osc) プロバイダーは、このインターフェイスを実装することができます。プロバイダーが、フレンドのオンデマンド同期、またはアクティビティのオンデマンド同期をサポートしている場合、またはキャッシュされた資格情報を使用してソーシャルネットワークにログオンしている場合です。 .osc プロバイダーが**ISocialSession2**を実装し、ソーシャルネットワークでフォローしているユーザーをサポートしている場合、.osc は i [alsession:: olperson](isocialsession-followperson.md)の代わりに[ISocialSession2:: olperson ex](isocialsession2-followpersonex.md)を呼び出し、プロバイダーが実装する必要があります。**ISocialSession2::** ということもあります。
  
## <a name="see-also"></a>関連項目

- [Outlook Social Connector プロバイダーインターフェイス](outlook-social-connector-provider-interfaces.md)

