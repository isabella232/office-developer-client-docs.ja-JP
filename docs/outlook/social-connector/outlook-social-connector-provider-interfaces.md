---
title: Outlook Social Connector プロバイダーインターフェイス
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8f92b2c7-9f47-4c84-874b-fec1a2a5b555
description: Outlook Social Connector (.osc) は、office クライアントアプリケーションによってソーシャルおよびビジネスネットワークに接続され、ユーザーが office を離れずにネットワーク内のユーザーと連絡を取り合うことができるようにする office の機能です。
ms.openlocfilehash: 77759db34f63239473e0682cfaca720860e96768
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359851"
---
# <a name="outlook-social-connector-provider-interfaces"></a>Outlook Social Connector プロバイダーインターフェイス

Outlook Social Connector (.osc) は、office クライアントアプリケーションによってソーシャルおよびビジネスネットワークに接続され、ユーザーが office を離れずにネットワーク内のユーザーと連絡を取り合うことができるようにする office の機能です。 
  
.osc プロバイダーは、コンポーネントオブジェクトモデル (COM) DLL で、各ソーシャルネットワークの api とは無関係に、.osc がソーシャルネットワークデータにアクセスできるようにします。 次の表に、.osc プロバイダ拡張機能のインターフェイスを示します。 .osc プロバイダーは、.osc と通信するために、次の5つのインターフェイスを実装する必要があります。 i入力された[alperson](isocialpersoniunknown.md)、 [i通達 alprofile](isocialprofileisocialperson.md)、 [isocialperson](isocialprovideriunknown.md)、および[i指定 alsession](isocialsessioniunknown.md)。 .osc プロバイダーが、フレンドの同期アクティビティ、オンデマンドまたはハイブリッド同期、ログイン資格情報のキャッシュ、キャッシュされた資格情報を使用したログオン、または個人をフォローする機能をサポートしている場合は、プロバイダーは ISocialSession2 を実装する必要があります。 [](isocialsession2iunknown.md)も同様です。
  
|**[名前]**|**[説明]**|
|:-----|:-----|
|[i社会](isocialpersoniunknown.md) <br/> |ソーシャルネットワーク上の人物を表します。  <br/> |
|[iこの alprofile](isocialprofileisocialperson.md) <br/> |ログオンしているユーザーを表します。  <br/> |
|[iこの alprovider](isocialprovideriunknown.md) <br/> |.osc プロバイダーのインスタンスを表します。  <br/> |
|[ISocialSession](isocialsessioniunknown.md) <br/> |ソーシャルネットワークサイトへの接続を表します。  <br/> |
|[ISocialSession2](isocialsession2iunknown.md) <br/> |アクティビティの同期、フレンドの追加、オンデマンドまたはハイブリッド同期、またはキャッシュされた資格情報を使用したソーシャルネットワークへのログオンをサポートします。  <br/> |
   

