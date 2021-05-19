---
title: サービス プロバイダーの一意の識別子の登録
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 964fceb4-8a1c-46c1-98e1-a325c9259f8b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9f4acbb06f85a88a6c057da263ae95e09f72e0bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410176"
---
# <a name="registering-service-provider-unique-identifiers"></a>サービス プロバイダーの一意の識別子の登録

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アドレス帳、メッセージ ストア、およびトランスポート プロバイダーは [、MAPIUID](mapiuid.md) と呼ばれる一意の識別子を使用して、さまざまな種類のサービス オブジェクトに登録します。 **MAPIUID は**、GUID を含む 16 バイトの識別子です。 MAPIUID は **、次の** 手順を使用して作成できます。 
  
1. 定数を定義します。
    
2. GUID の作成Visual Studio *ツールを呼び* 出します。 
    
たとえば、アドレス帳プロバイダーは、MAPIUID を定義するヘッダー ファイルに次の定数 **を含める場合があります**。
  
 `#define AB_UID_PROVIDER { 0Xe3, 0x3c, 0x67, 0xa0, \ 0xc8, 0x1f, 0x11, 0xce, \ 0xb2, 0xe4, 0x0, 0xaa, \ 0x0, 0x51, 0xe, 0x3b }`
  
 **プロバイダーがアドレス帳またはメッセージ ストア プロバイダーの場合に MAPIUID を登録するには**
  
1. [IMAPISupport::SetProviderUID を呼び出します](imapisupport-setprovideruid.md)。
    
2. インスタンス化するログオン オブジェクトごとに MAPIUID を登録し、作成する各エントリ識別子の ab メンバーの最初の 16 バイトにこの **MAPIUID** を含めます。  MAPI は **MAPIUID 構造を使用** して、オブジェクトをサービス プロバイダーに関連付ける。 クライアントが [IMAPISession::OpenEntry](imapisession-openentry.md) メソッドを呼び出してオブジェクトを開く場合、MAPI はエントリ識別子の **MAPIUID** 部分を調べ、登録されている **MAPIUID** と照合して、開いている要求を受け取るログオン オブジェクトを決定します。
    
3. プロバイダーがトランスポートの場合は、MAPI が **IXPLogon::AddressTypes** メソッドを呼び出す際に、1 つ以上の **MAPIUID** 構造体を登録します。 MAPI は、トランスポート プロバイダーによって登録された **MAPIUID** 構造を使用して、メッセージ配信の責任を割り当てします。 
    
サービス プロバイダーは通常、1 つの **MAPIUID** を登録しますが、複数の **MAPIUID 構造体を登録** できます。 アドレス帳またはメッセージ ストア プロバイダーが複数のログオン オブジェクトをサポートしている場合 (たとえば、ユーザーがプロバイダーの複数のインスタンスをプロファイルに追加できる場合など)、ログオン オブジェクトごとに異なる **MAPIUID** を実装できます。 複数の **MAPIUID** をサポートする他のいくつかの理由があります。
  
- 複数のバージョンのプロバイダーをサポートする必要があります。エントリ識別子は適切なバージョンを表す必要があります。 バージョンごとに **異なる MAPIUID** を割り当てる。 
    
- サポートするオブジェクトの種類を区別する必要があります。 たとえば、アドレス帳プロバイダーは、メッセージング ユーザー オブジェクトのエントリ識別子で使用する **MAPIUID** を 1 つ登録し、配布リストに使用する別の **MAPIUID** を登録する場合があります。 
    
同時にアクティブなログオン オブジェクトが複数ある場合は、それぞれ固有の **MAPIUID** 構造を持つ必要があります。 これにより、MAPI がエントリ識別子とサービス プロバイダーに一致する精度が向上し、一部の作業時間が節約されます。 すべてのログオン オブジェクトに固有の識別子がある場合、MAPI はログオン オブジェクトにルーティングする要求をそのオブジェクトで処理できます。 ログオン オブジェクトが **MAPIUID** 構造を共有する場合、MAPI は MAPIUID によって識別される最初のログオン オブジェクトに **要求をルーティングします**。 エントリ識別子を処理しないので処理できない要求をログオン オブジェクトの 1 つが受信した場合は、エラーを返す前に、次のログオン オブジェクトに要求を渡します。
  
## <a name="see-also"></a>関連項目



[サービス プロバイダー ログオンの実装](implementing-service-provider-logon.md)

