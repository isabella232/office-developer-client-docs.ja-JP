---
title: トランスポート オーダを設定
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4a140ec3-9520-4119-a975-0fb6c1049967
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 71d7ebf2bc8c7bbf3b5ee6ce60959fdeee79abe3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803895"
---
# <a name="setting-transport-order"></a>トランスポート オーダを設定

  
  
**適用されます**: Outlook 
  
MAPI スプーラーに送信メッセージを処理できるトランスポート プロバイダーを宣言するための識別子とアドレスの種類に基づく責任が割り当てられます。 トランスポート プロバイダーがサポートされているアドレスの種類と識別子のリストを発行する- **MAPIUID**構造体に格納されている: MAPI がログオンの直後に、 [IXPLogon::AddressTypes](ixplogon-addresstypes.md)メソッドを呼び出すとします。 受信者のアドレスの種類は、 **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) プロパティに格納されます。
  
アドレスの種類を登録することを示します MAPI トランスポート プロバイダーは、登録されているアドレスの種類を設定、 **PR_ADDRTYPE**プロパティを使用して受信者に配信できること。 同様にの**MAPIUID**に登録するには、トランスポート プロバイダーが登録されている**MAPIUID**のエントリの識別子によって表される受信者に提供できることを示します。
  
ほとんどのトランスポート プロバイダーの登録の 1 つまたは複数のアドレスの種類です。数は、 **MAPIUID**で登録します。 アドレス帳プロバイダーと密に結合し、そのエントリの識別子の形式を理解するためのトランスポート プロバイダーは、 **MAPIUID**、それによってパフォーマンスの向上によってメッセージを処理するために登録できます。 このような密結合のトランスポート プロバイダーから抽出できます、受信者の電子メール アドレスおよびその他の必要な情報のエントリ id、 **IMAPISupport::OpenEntry**の呼び出しを使用してそれを開くことがなく。 
  
MAPI は、トランスポート プロバイダーは、複数のトランスポート プロバイダーは、同じアドレスの種類または**MAPIUID**に登録しているときに使用される順序が維持されます。 [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)を呼び出すことによって、この順序を上書きすることができ、 _lpUIDList_パラメーターで指定されたすべてのアクティブなトランスポート プロバイダーの**MAPIUID**s の順序付きリストを渡すことです。。 
  
アクティブなトランスポート プロバイダーの 1 つで処理可能なアドレスの種類のすべての一覧を取得するには、 [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md)を呼び出します。 **EnumAdrTypes**は、現在のセッションでアクティブになっているトランスポート プロバイダーによってサポートされているアドレスの種類を説明する文字列の配列を返します。 
  

