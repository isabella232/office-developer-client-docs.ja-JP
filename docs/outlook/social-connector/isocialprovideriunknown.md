---
title: ISocialProvider IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 1c9f4dd4-65f6-446f-8b86-a375ce402658
description: ソーシャル コネクタ (OSC) Outlookのインスタンスを表します。
ms.openlocfilehash: b784ce945988c983d28d93fd351bb2d10b4e48ec
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583010"
---
# <a name="isocialprovider--iunknown"></a>ISocialProvider : IUnknown

ソーシャル コネクタ (OSC) Outlookのインスタンスを表します。
  
## <a name="members"></a>メンバー

次の表に **、ISocialProvider** インターフェイスで使用できるメンバーを示します。 
  
|**名前**|**メンバーの種類**|**説明**|
|:-----|:-----|:-----|
|[DefaultSiteUrls](isocialprovider-defaultsiteurls.md) <br/> |プロパティ  <br/> |OSC プロバイダーのサイト URL を指定する文字列の配列を返します。  <br/> |
|[GetAutoConfiguredSession](isocialprovider-getautoconfiguredsession.md) <br/> |Method  <br/> |自動構成された [ISocialSession](isocialsessioniunknown.md) インターフェイスを取得します。  <br/> |
|[GetCapabilities](isocialprovider-getcapabilities.md) <br/> |Method  <br/> |プロバイダーの機能を説明する文字列を取得します。  <br/> |
|[GetSession](isocialprovider-getsession.md) <br/> |Method  <br/> |[ISocialSession インターフェイスを取得](isocialsessioniunknown.md)します。  <br/> |
|[GetStatusSettings](isocialprovider-getstatussettings.md) <br/> |Method  <br/> |このメソッドは現在サポートされていません。  <br/> |
|[Load](isocialprovider-load.md) <br/> |Method  <br/> |OSC プロバイダーを初期化します。  <br/> |
|[SocialNetworkGuid](isocialprovider-socialnetworkguid.md) <br/> |プロパティ  <br/> |ソーシャル ネットワークの一意の識別子を表す GUID を返します。  <br/> |
|[SocialNetworkIcon](isocialprovider-socialnetworkicon.md) <br/> |プロパティ  <br/> |ソーシャル ネットワークのアイコンを表すバイトの配列を返します。  <br/> |
|[SocialNetworkName](isocialprovider-socialnetworkname.md) <br/> |プロパティ  <br/> |ソーシャル ネットワーク名を表す文字列を返します。  <br/> |
|[バージョン](isocialprovider-version.md) <br/> |プロパティ  <br/> |このソーシャル ネットワークのプロバイダーのバージョン番号を表す文字列を返します。  <br/> |
   
## <a name="remarks"></a>注釈

OSC プロバイダーは、OSC と通信するためにこのインターフェイスを実装する必要があります。
  
## <a name="see-also"></a>関連項目

- [Outlookソーシャル コネクタ プロバイダー インターフェイス](outlook-social-connector-provider-interfaces.md)

