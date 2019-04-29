---
title: トランスポート順序の設定
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4a140ec3-9520-4119-a975-0fb6c1049967
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: efa2d6ab9edbd50634093b5185ef9036689f1379
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433599"
---
# <a name="setting-transport-order"></a>トランスポート順序の設定

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI スプーラーは、トランスポートプロバイダーが処理できる、アドレスの種類と識別子に基づいて、送信メッセージの責任を割り当てます。 トランスポートプロバイダーは、 **MAPIUID**構造に格納されているサポートされているアドレスの種類と識別子の一覧を発行します。これは、MAPI が[IXPLogon:: AddressTypes](ixplogon-addresstypes.md)メソッドをログオンした直後に呼び出したときに行います。 受信者のアドレスの種類は、その**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) プロパティに格納されます。
  
アドレスの種類を登録すると、トランスポートプロバイダーは、 **PR_ADDRTYPE**プロパティが登録されているアドレスの種類に設定された受信者に配信できる MAPI に示されます。 同様に、 **MAPIUID**の登録は、トランスポートプロバイダーが登録済みの**MAPIUID**を持つエントリ id で表される受信者に配信できることを示します。
  
ほとんどのトランスポートプロバイダーは、1つまたは複数のアドレスの種類に対して登録します。**MAPIUID**による登録はほとんどありません。 アドレス帳プロバイダーと密接に結合され、そのエントリ識別子形式を理解しているトランスポートプロバイダーは、 **MAPIUID**によってメッセージを処理するように登録できます。これにより、パフォーマンスが向上します。 これらの密結合トランスポートプロバイダーは、受信者の電子メールアドレスやその他の必要な情報を**imapisupport:: openentry**呼び出しを使用して開くことなく、エントリ識別子から抽出できます。 
  
MAPI は、複数のトランスポートプロバイダーが同じアドレスの種類または**MAPIUID**に登録されている場合に使用されるトランスポートプロバイダーの順序を保持します。 この順序を上書きするには、 [IMsgServiceAdmin:: msgservicetransportorder](imsgserviceadmin-msgservicetransportorder.md)を呼び出し、 _lpuidlist_パラメーターで示されているすべてのアクティブなトランスポートプロバイダーの**MAPIUID**s の順序付きリストを渡します。 
  
アクティブなトランスポートプロバイダーのいずれかによって処理可能なすべてのアドレスの種類の一覧を取得するには、 [imapisession:: enumadrtypes](imapisession-enumadrtypes.md)を呼び出します。 **enumadrtypes**は、現在のセッションでアクティブなトランスポートプロバイダーによってサポートされているアドレスの種類を表す文字列の配列を返します。 
  

