---
title: iこの alprovider IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1c9f4dd4-65f6-446f-8b86-a375ce402658
description: Outlook Social Connector (.osc) プロバイダーのインスタンスを表します。
ms.openlocfilehash: f28b8343d92b09455b6049f421b839efbda21c1a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285485"
---
# <a name="isocialprovider--iunknown"></a>ISocialProvider : IUnknown

Outlook Social Connector (.osc) プロバイダーのインスタンスを表します。
  
## <a name="members"></a>Members

次の表に、 **iare alprovider**インターフェイスで使用できるメンバーを示します。 
  
|**Name**|**メンバーの種類**|**説明**|
|:-----|:-----|:-----|
|[defaultsiteurls](isocialprovider-defaultsiteurls.md) <br/> |プロパティ  <br/> |.osc プロバイダーのサイト url を指定する文字列の配列を返します。  <br/> |
|[GetAutoConfiguredSession](isocialprovider-getautoconfiguredsession.md) <br/> |メソッド  <br/> |自動構成された [ISocialSession](isocialsessioniunknown.md) インターフェイスを取得します。  <br/> |
|[GetCapabilities](isocialprovider-getcapabilities.md) <br/> |メソッド  <br/> |プロバイダー機能について説明する文字列を取得します。  <br/> |
|[getsession](isocialprovider-getsession.md) <br/> |メソッド  <br/> |i式[alsession](isocialsessioniunknown.md)インターフェイスを取得します。  <br/> |
|[getstatussettings](isocialprovider-getstatussettings.md) <br/> |メソッド  <br/> |このメソッドは現在サポートされていません。  <br/> |
|[Load](isocialprovider-load.md) <br/> |メソッド  <br/> |.osc プロバイダーを初期化します。  <br/> |
|["/ネットワーク guid"](isocialprovider-socialnetworkguid.md) <br/> |プロパティ  <br/> |ソーシャルネットワークの一意の識別子を表す GUID を返します。  <br/> |
|["/ネットワーク] アイコン](isocialprovider-socialnetworkicon.md) <br/> |プロパティ  <br/> |ソーシャルネットワークのアイコンを表すバイト配列を返します。  <br/> |
|[指定した仮のネットワーク名](isocialprovider-socialnetworkname.md) <br/> |プロパティ  <br/> |ソーシャルネットワーク名を表す文字列を返します。  <br/> |
|[バージョン](isocialprovider-version.md) <br/> |プロパティ  <br/> |このソーシャルネットワークのプロバイダーのバージョン番号を表す文字列を返します。  <br/> |
   
## <a name="remarks"></a>解説

.osc プロバイダーは、このインターフェイスを実装して、.osc と通信する必要があります。
  
## <a name="see-also"></a>関連項目

- [Outlook Social Connector プロバイダーインターフェイス](outlook-social-connector-provider-interfaces.md)

