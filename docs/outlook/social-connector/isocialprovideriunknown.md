---
title: ISocialProvider IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1c9f4dd4-65f6-446f-8b86-a375ce402658
description: Outlook ソーシャル コネクタ (OSC) プロバイダーのインスタンスを表します。
ms.openlocfilehash: 912b2d92137febe80e0d97362e0a490f138b2e66
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804479"
---
# <a name="isocialprovider--iunknown"></a>ISocialProvider: IUnknown

Outlook ソーシャル コネクタ (OSC) プロバイダーのインスタンスを表します。
  
## <a name="members"></a>メンバー

次の表は、 **ISocialProvider**インターフェイスで使用可能なメンバーを示します。 
  
|**名前**|**メンバーの種類**|**説明**|
|:-----|:-----|:-----|
|[DefaultSiteUrls](isocialprovider-defaultsiteurls.md) <br/> |Property  <br/> |OSC プロバイダーのサイトの Url を指定する文字列の配列を返します。  <br/> |
|[GetAutoConfiguredSession](isocialprovider-getautoconfiguredsession.md) <br/> |メソッド  <br/> |自動的に構成されている[ISocialSession](isocialsessioniunknown.md)インターフェイスを取得します。  <br/> |
|[GetCapabilities](isocialprovider-getcapabilities.md) <br/> |メソッド  <br/> |プロバイダーの機能を説明する文字列を取得します。  <br/> |
|[GetSession](isocialprovider-getsession.md) <br/> |メソッド  <br/> |[ISocialSession](isocialsessioniunknown.md)インターフェイスを取得します。  <br/> |
|[GetStatusSettings](isocialprovider-getstatussettings.md) <br/> |メソッド  <br/> |このメソッドは現在サポートされていません。  <br/> |
|[Load](isocialprovider-load.md) <br/> |メソッド  <br/> |OSC プロバイダーを初期化します。  <br/> |
|[SocialNetworkGuid](isocialprovider-socialnetworkguid.md) <br/> |Property  <br/> |ソーシャル ネットワークの一意の識別子を表す GUID を返します。  <br/> |
|[SocialNetworkIcon](isocialprovider-socialnetworkicon.md) <br/> |Property  <br/> |ソーシャル ネットワークのアイコンを表すバイトの配列を返します。  <br/> |
|[SocialNetworkName](isocialprovider-socialnetworkname.md) <br/> |Property  <br/> |ソーシャル ネットワーク名を表す文字列を返します。  <br/> |
|[バージョン](isocialprovider-version.md) <br/> |Property  <br/> |このソーシャル ネットワーク プロバイダーのバージョン番号を表す文字列を返します。  <br/> |
   
## <a name="remarks"></a>備考

OSC プロバイダーでは、OSC と通信するには、このインターフェイスを実装する必要があります。
  
## <a name="see-also"></a>関連項目

- [Outlook ソーシャル コネクタ プロバイダー インターフェイス](outlook-social-connector-provider-interfaces.md)

