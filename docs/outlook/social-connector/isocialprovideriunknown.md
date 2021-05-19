---
title: ISocialProvider IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1c9f4dd4-65f6-446f-8b86-a375ce402658
description: ソーシャル コネクタ (OSC) Outlookのインスタンスを表します。
ms.openlocfilehash: f28b8343d92b09455b6049f421b839efbda21c1a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409959"
---
# <a name="isocialprovider--iunknown"></a>ISocialProvider : IUnknown

ソーシャル コネクタ (OSC) Outlookのインスタンスを表します。
  
## <a name="members"></a>Members

次の表に **、ISocialProvider** インターフェイスで使用できるメンバーを示します。 
  
|**名前**|**メンバーの種類**|**説明**|
|:-----|:-----|:-----|
|[DefaultSiteUrls](isocialprovider-defaultsiteurls.md) <br/> |プロパティ  <br/> |OSC プロバイダーのサイト URL を指定する文字列の配列を返します。  <br/> |
|[GetAutoConfiguredSession](isocialprovider-getautoconfiguredsession.md) <br/> |メソッド  <br/> |自動構成された [ISocialSession](isocialsessioniunknown.md) インターフェイスを取得します。  <br/> |
|[GetCapabilities](isocialprovider-getcapabilities.md) <br/> |メソッド  <br/> |プロバイダーの機能を説明する文字列を取得します。  <br/> |
|[GetSession](isocialprovider-getsession.md) <br/> |メソッド  <br/> |[ISocialSession インターフェイスを取得](isocialsessioniunknown.md)します。  <br/> |
|[GetStatusSettings](isocialprovider-getstatussettings.md) <br/> |メソッド  <br/> |このメソッドは現在サポートされていません。  <br/> |
|[Load](isocialprovider-load.md) <br/> |メソッド  <br/> |OSC プロバイダーを初期化します。  <br/> |
|[SocialNetworkGuid](isocialprovider-socialnetworkguid.md) <br/> |プロパティ  <br/> |ソーシャル ネットワークの一意の識別子を表す GUID を返します。  <br/> |
|[SocialNetworkIcon](isocialprovider-socialnetworkicon.md) <br/> |プロパティ  <br/> |ソーシャル ネットワークのアイコンを表すバイトの配列を返します。  <br/> |
|[SocialNetworkName](isocialprovider-socialnetworkname.md) <br/> |プロパティ  <br/> |ソーシャル ネットワーク名を表す文字列を返します。  <br/> |
|[バージョン](isocialprovider-version.md) <br/> |プロパティ  <br/> |このソーシャル ネットワークのプロバイダーのバージョン番号を表す文字列を返します。  <br/> |
   
## <a name="remarks"></a>注釈

OSC プロバイダーは、OSC と通信するためにこのインターフェイスを実装する必要があります。
  
## <a name="see-also"></a>関連項目

- [Outlookソーシャル コネクタ プロバイダー インターフェイス](outlook-social-connector-provider-interfaces.md)

