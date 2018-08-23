---
title: Outlook ソーシャル コネクタ プロバイダー インターフェイス
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8f92b2c7-9f47-4c84-874b-fec1a2a5b555
description: Outlook ソーシャル コネクタ (OSC) では、Office 機能 Office クライアント アプリケーションで共有社会に接続して、ビジネス ネットワークは、Office を離れることがなく、ネットワーク内のユーザーをユーザーが維持できるようにするためです。
ms.openlocfilehash: bc393f32e563bbbef70538ea00cd92cf7f96729c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804456"
---
# <a name="outlook-social-connector-provider-interfaces"></a>Outlook ソーシャル コネクタ プロバイダー インターフェイス

Outlook ソーシャル コネクタ (OSC) では、Office 機能 Office クライアント アプリケーションで共有社会に接続して、ビジネス ネットワークは、Office を離れることがなく、ネットワーク内のユーザーをユーザーが維持できるようにするためです。 
  
OSC プロバイダーでは、コンポーネント オブジェクト モデル (COM) DLL の各ソーシャル ネットワークの Api に依存しない方法でデータをソーシャル ネットワークにアクセスする OSC を可能にします。 次の表は、OSC プロバイダーの拡張機能でインターフェイスを一覧表示します。 OSC プロバイダーは、OSC と通信するのには 5 つのインタ フェースの 4 つを実装する必要が: [ISocialPerson](isocialpersoniunknown.md)、 [ISocialProfile](isocialprofileisocialperson.md)、 [ISocialProvider](isocialprovideriunknown.md)、および[ISocialSession](isocialsessioniunknown.md)。 OSC プロバイダーは、同期アクティビティ、オン ・ デマンドをサポートしている場合、または資格情報、または個人を追跡する機能にキャッシュされたログオン資格情報をキャッシュしを使用してログオンするときに、友人のハイブリッド同期プロバイダーは、 [ISocialSession2 を実装する必要があります。](isocialsession2iunknown.md)も同様です。
  
|**名前**|**説明**|
|:-----|:-----|
|[ISocialPerson](isocialpersoniunknown.md) <br/> |ソーシャル ネットワーク上のユーザーを表します。  <br/> |
|[ISocialProfile](isocialprofileisocialperson.md) <br/> |ユーザーのログオンを表します。  <br/> |
|[ISocialProvider](isocialprovideriunknown.md) <br/> |OSC プロバイダーのインスタンスを表します。  <br/> |
|[ISocialSession](isocialsessioniunknown.md) <br/> |ソーシャル ネットワーク サイトへの接続を表します。  <br/> |
|[ISocialSession2](isocialsession2iunknown.md) <br/> |友人を追加する、アクティビティの同期をサポートするオン ・ デマンドまたはハイブリッドの同期の友人、またはを使用して、ソーシャル ネットワークへのログオンにキャッシュされた資格情報。  <br/> |
   

