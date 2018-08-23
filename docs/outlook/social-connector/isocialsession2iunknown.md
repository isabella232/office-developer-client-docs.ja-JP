---
title: ISocialSession2 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f516e86e-0158-472b-9711-fe7491b24404
description: キャッシュされた資格情報を使用して、友人、友人の同期をオン ・ デマンドまたはハイブリッド、活動、またはソーシャル ネットワークへのログオンのオンデマンドの同期を追加することをサポートします。
ms.openlocfilehash: b14804d35e54ebe9fe2a529fb2664f0a661653bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804376"
---
# <a name="isocialsession2--iunknown"></a>ISocialSession2 : IUnknown

キャッシュされた資格情報を使用して、友人、友人の同期をオン ・ デマンドまたはハイブリッド、活動、またはソーシャル ネットワークへのログオンのオンデマンドの同期を追加することをサポートします。
  
## <a name="members"></a>Members

次の表は、 **ISocialSession2**インターフェイスで使用可能なメンバーを示します。 
  
|**名前**|**メンバーの種類**|**説明**|
|:-----|:-----|:-----|
|[FollowPersonEx](isocialsession2-followpersonex.md) <br/> |メソッド  <br/> |ソーシャル ネットワークにログオン中のユーザーのフレンドとして、 _emailAddresses_パラメーターと_displayName_パラメーターで識別されるユーザーを追加します。  <br/> |
|[GetActivitiesEx](isocialsession2-getactivitiesex.md) <br/> |メソッド  <br/> |_HashedAddresses_パラメーターで指定されたユーザーのアクティビティのコレクションを表す文字列を取得します。  <br/> |
|[GetPeopleDetails](isocialsession2-getpeopledetails.md) <br/> |メソッド  <br/> |_PersonsAddresses_パラメーターで指定されたユーザーのユーザーと画像の詳細情報のコレクションを格納する文字列を返します。  <br/> |
|[LogonCached](isocialsession2-logoncached.md) <br/> |メソッド  <br/> |キャッシュされた資格情報を使用して、ソーシャル ネットワーク サイトにログオンします。  <br/> |
   
## <a name="remarks"></a>注釈

プロバイダーがキャッシュされた資格情報を使用して、友人のオン ・ デマンドまたはハイブリッドの同期、オンデマンドの同期活動、またはソーシャル ネットワークへのログオンをサポートしている場合、このインターフェイスを実装するために、Outlook ソーシャル コネクタ (OSC) プロバイダーを選択できます。 OSC プロバイダーは、 **ISocialSession2**と次の人をソーシャル ネットワークのサポートを実装する場合は、OSC では、 [ISocialSession::FollowPerson](isocialsession-followperson.md)、代わりに[ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md)を呼び出して、プロバイダーを実装する必要があります。**ISocialSession2::FollowPersonEx**も同様です。
  
## <a name="see-also"></a>関連項目

- [Outlook ソーシャル コネクタ プロバイダー インターフェイス](outlook-social-connector-provider-interfaces.md)

