---
title: Outlookソーシャル コネクタ プロバイダー インターフェイス
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 8f92b2c7-9f47-4c84-874b-fec1a2a5b555
description: Outlook ソーシャル コネクタ (OSC) は、Office クライアント アプリケーションが共有する Office 機能で、ソーシャル ネットワークやビジネス ネットワークに接続し、ユーザーが Office を離れることなくネットワーク内のユーザーと連絡を取り合える機能です。
ms.openlocfilehash: d45928fe371a69f5fa47a7b78cb2da7a9e49249b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566123"
---
# <a name="outlook-social-connector-provider-interfaces"></a>Outlookソーシャル コネクタ プロバイダー インターフェイス

Outlook ソーシャル コネクタ (OSC) は、Office クライアント アプリケーションが共有する Office 機能で、ソーシャル ネットワークやビジネス ネットワークに接続し、ユーザーが Office を離れることなくネットワーク内のユーザーと連絡を取り合える機能です。 
  
OSC プロバイダーはコンポーネント オブジェクト モデル (COM) DLL で、各ソーシャル ネットワークの API とは独立した方法で OSC がソーシャル ネットワーク データにアクセスできます。 次の表に、OSC プロバイダーの機能拡張のインターフェイスを示します。 OSC プロバイダーは、5 つのインターフェイスの 4 つを実装して OSC と通信する必要があります[。ISocialPerson](isocialpersoniunknown.md) [、ISocialProfile、ISocialProvider、](isocialprofileisocialperson.md)[および ISocialSession](isocialsessioniunknown.md)です。 [](isocialprovideriunknown.md) OSC プロバイダーがアクティビティの同期、フレンドのオンデマンドまたはハイブリッド同期、ログオン資格情報のキャッシュ、キャッシュされた資格情報の使用、またはユーザーのフォロー機能をサポートしている場合、プロバイダーは [ISocialSession2](isocialsession2iunknown.md)も実装する必要があります。
  
|**名前**|**説明**|
|:-----|:-----|
|[ISocialPerson](isocialpersoniunknown.md) <br/> |ソーシャル ネットワーク上のユーザーを表します。  <br/> |
|[ISocialProfile](isocialprofileisocialperson.md) <br/> |ログオンしているユーザーを表します。  <br/> |
|[ISocialProvider](isocialprovideriunknown.md) <br/> |OSC プロバイダーのインスタンスを表します。  <br/> |
|[ISocialSession](isocialsessioniunknown.md) <br/> |ソーシャル ネットワーク サイトへの接続を表します。  <br/> |
|[ISocialSession2](isocialsession2iunknown.md) <br/> |キャッシュされた資格情報を使用して、アクティビティの同期、友人の追加、フレンドのオンデマンドまたはハイブリッド同期、またはソーシャル ネットワークへのログオンをサポートします。  <br/> |
   

