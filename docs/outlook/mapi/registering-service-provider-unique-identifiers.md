---
title: サービス プロバイダー一意識別子の登録
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 964fceb4-8a1c-46c1-98e1-a325c9259f8b
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 80d2e4fd353f0746349563fd911e0af09a658b35
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803737"
---
# <a name="registering-service-provider-unique-identifiers"></a>サービス プロバイダー一意識別子の登録

  
  
**適用対象**: Outlook 
  
アドレス帳、メッセージ ・ ストア、およびトランスポート プロバイダーは、さまざまな種類のサービス オブジェクトを登録するのには、 [MAPIUID](mapiuid.md)と呼ばれる一意の識別子を使用します。 の**MAPIUID**は、GUID を格納する 16 バイトの識別子です。 次の手順を使用して、 **MAPIUID**を作成します。 
  
1. 定数を定義します。
    
2. Visual Studio の *[GUID の作成*を呼び出す * ツールです。 
    
たとえば、アドレス帳プロバイダーとの**MAPIUID**を定義するヘッダー ファイルに次の定数場合があります。
  
 `#define AB_UID_PROVIDER { 0Xe3, 0x3c, 0x67, 0xa0, \ 0xc8, 0x1f, 0x11, 0xce, \ 0xb2, 0xe4, 0x0, 0xaa, \ 0x0, 0x51, 0xe, 0x3b }`
  
 **プロバイダーがアドレス帳またはメッセージ ストア プロバイダーの場合、MAPIUID を登録するのには**
  
1. [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)を呼び出します。
    
2. 各ログオン用の**MAPIUID**を登録するオブジェクトのインスタンスを作成して、 **ab**のメンバーを作成するすべてのエントリの識別子の最初の 16 バイトにこの**MAPIUID**が含まれます。 MAPI は、サービス プロバイダーとオブジェクトを関連付けるには、 **MAPIUID**構造体を使用します。 開くには、MAPI オブジェクトの[IMAPISession::OpenEntry](imapisession-openentry.md)メソッドは、 **MAPIUID**の部分のエントリ id を調べ、クライアント呼び出しに対して、登録されている**MAPIUID**、ログオン オブジェクトを決定することと一致する必要がありますが表示される、開く要求します。
    
3. プロバイダーが、トランスポートの場合は、MAPI は、 **IXPLogon::AddressTypes**メソッドを呼び出すと、1 つまたは複数の**MAPIUID**構造体を登録します。 MAPI は、メッセージ配信のための責任を割り当てるには、トランスポート プロバイダーが登録されている**MAPIUID**構造体を使用します。 
    
サービス プロバイダーは、通常、1 つの**MAPIUID**を登録するが、複数の**MAPIUID**構造体を登録できます。 場合は、アドレス帳やメッセージ ストア プロバイダーをサポートしています複数のログオン オブジェクトでは、おそらく、プロファイルには、プロバイダーの複数のインスタンスを追加するユーザーを許可して、ログオン オブジェクトごとに別の**MAPIUID**を実装する可能性があります。 複数の**MAPIUID**をサポートするその他の理由はいくつかあります。
  
- プロバイダーの複数のバージョンをサポートする必要があり、エントリ id は適切なバージョンを表す必要があります。 バージョンごとに別の**MAPIUID**を割り当てます。 
    
- サポートするオブジェクトの種類を区別するには。 たとえば、アドレス帳プロバイダーは 1 つの**MAPIUID**でのメッセージングのユーザー オブジェクトのエントリ id を使用して配布リストを使用する別の**MAPIUID**を登録する可能性があります。 
    
同時にアクティブになっている複数のログオン オブジェクトが存在する場合、合理的ごとに一意の**MAPIUID**構造体を持つ。 MAPI サービス プロバイダーへのエントリの識別子と一致していくつかの作業を保存する精度が向上します。 すべてログオン オブジェクトでは、独自の一意の識別子を持っていると、MAPI ことを保証できるいずれかの要求をログオン オブジェクトへのルートは、そのオブジェクトで処理できます。 ログオン オブジェクトでは、 **MAPIUID**構造体を共有している場合、MAPI は**MAPIUID**によって識別される最初のログオン オブジェクトに要求をルーティングします。 ログオン オブジェクトの 1 つは、エントリの識別子を処理しないために処理できない要求を受信する場合は、エラーを返す前に、次のログオン オブジェクトに要求を渡します。
  
## <a name="see-also"></a>関連項目



[サービス プロバイダー ログオンの実装](implementing-service-provider-logon.md)

