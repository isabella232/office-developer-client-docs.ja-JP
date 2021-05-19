---
title: トランスポートの順序の設定
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
# <a name="setting-transport-order"></a>トランスポートの順序の設定

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI スプーラーは、トランスポート プロバイダーが処理できると宣言するアドレスの種類と識別子に基づいて、送信メッセージの責任を割り当てします。 トランスポート プロバイダーは、MAPI がログオン直後に [IXPLogon::AddressTypes](ixplogon-addresstypes.md)メソッドを呼び出す場合に **、MAPIUID** 構造に格納されているサポートされているアドレスの種類と識別子の一覧を公開します。 受信者のアドレスの種類は、プロパティ ([PidTagAddressType](pidtagaddresstype-canonical-property.md) **)** PR_ADDRTYPEに格納されます。
  
アドレスの種類に登録すると、トランスポート プロバイダーは、登録されているアドレスの種類に設定された PR_ADDRTYPE プロパティを使用して **受信者** に配信できる MAPI を示します。 同様に **、MAPIUID** を登録すると、トランスポート プロバイダーは、登録済みの **MAPIUID** を持つエントリ識別子によって表される受信者に配信できます。
  
ほとんどのトランスポート プロバイダーは、1 つ以上のアドレスの種類に登録します。 **MAPIUID による登録が少ない**。 アドレス帳プロバイダーと緊密に結合され、そのエントリ識別子の形式を理解しているトランスポート プロバイダーは **、MAPIUID** によってメッセージを処理するために登録でき、パフォーマンスが向上します。 これらの緊密に結合されたトランスポート プロバイダーは **、IMAPISupport::OpenEntry** 呼び出しで開かなくても、受信者の電子メール アドレスなどの必要な情報をエントリ識別子から抽出できます。 
  
MAPI は、複数のトランスポート プロバイダーが同じアドレスの種類または MAPIUID に登録されている場合に使用されるトランスポート プロバイダーの **注文を維持します**。 この順序をオーバーライドするには [、IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)を呼び出し _、lpUIDList_ パラメーターが指すすべてのアクティブなトランスポート プロバイダーの **MAPIUID** の順序付きリストを渡します。 
  
アクティブなトランスポート プロバイダーの 1 つで処理できるすべてのアドレスの種類の一覧を取得するには [、IMAPISession::EnumAdrTypes を呼び出します](imapisession-enumadrtypes.md)。 **EnumAdrTypes** は、現在のセッションでアクティブなトランスポート プロバイダーがサポートするアドレスの種類を表す文字列の配列を返します。 
  

