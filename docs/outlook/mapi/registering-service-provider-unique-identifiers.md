---
title: サービスプロバイダーの一意識別子の登録
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
# <a name="registering-service-provider-unique-identifiers"></a>サービスプロバイダーの一意識別子の登録

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アドレス帳、メッセージストア、およびトランスポートプロバイダーは、 [MAPIUID](mapiuid.md)と呼ばれる一意の識別子を使用して、さまざまな種類のサービスオブジェクトに登録します。 **MAPIUID**は、GUID を含む16バイトの識別子です。 次の手順を使用して、 **MAPIUID**を作成できます。 
  
1. 定数を定義します。
    
2. Visual Studio の [*GUID の作成*] ツールを起動します。 
    
たとえば、アドレス帳プロバイダーでは、 **MAPIUID**を定義するために、ヘッダーファイルに次の定数を含めることができます。
  
 `#define AB_UID_PROVIDER { 0Xe3, 0x3c, 0x67, 0xa0, \ 0xc8, 0x1f, 0x11, 0xce, \ 0xb2, 0xe4, 0x0, 0xaa, \ 0x0, 0x51, 0xe, 0x3b }`
  
 **プロバイダーがアドレス帳またはメッセージストアプロバイダーの場合に MAPIUID を登録するには**
  
1. Call [imapisupport:: setprovideruid](imapisupport-setprovideruid.md)。
    
2. インスタンス化された各ログオンオブジェクトに対して**MAPIUID**を登録し、作成するすべてのエントリ識別子の**ab**メンバーの最初の16バイトにこの**MAPIUID**を含めます。 MAPI では、 **MAPIUID**構造を使用してオブジェクトをサービスプロバイダーに関連付けます。 クライアントが[imapisession:: openentry](imapisession-openentry.md)メソッドを呼び出してオブジェクトを開くと、MAPI はエントリ識別子の**MAPIUID**部分を調べ、登録されている**MAPIUID**と照合して、開いているログオンオブジェクトを特定します。タキ.
    
3. プロバイダーがトランスポートの場合は、MAPI が**IXPLogon:: AddressTypes**メソッドを呼び出すときに1つ以上の**MAPIUID**構造体を登録します。 MAPI は、トランスポートプロバイダーによって登録された**MAPIUID**構造を使用して、メッセージ配信の責任を割り当てます。 
    
通常、サービスプロバイダーは1つの**MAPIUID**を登録しますが、複数の**MAPIUID**構造体を登録することは可能です。 ユーザーが自分のプロファイルにプロバイダーの複数のインスタンスを追加することを許可することによって、アドレス帳またはメッセージストアプロバイダーが複数のログオンオブジェクトをサポートしている場合は、各ログオンオブジェクトに異なる**MAPIUID**を実装することをお勧めします。 複数の**MAPIUID**をサポートする理由は、他にもいくつかあります。
  
- プロバイダーの複数のバージョンをサポートする必要があります。また、エントリ識別子は適切なバージョンを表す必要があります。 各バージョンに異なる**MAPIUID**を割り当てます。 
    
- サポートするオブジェクトの種類を区別する場合。 たとえば、アドレス帳プロバイダーは、メッセージングユーザーオブジェクトのエントリ識別子で使用する1つの**MAPIUID**と、配布リストに使用する別の**MAPIUID**を登録する必要があります。 
    
同時にアクティブな複数のログオンオブジェクトがある場合は、それぞれに固有の**MAPIUID**構造があるという意味になります。 これにより、MAPI がサービスプロバイダーにエントリ識別子を一致させ、一部の作業を節約できるため、精度が向上します。 すべてのログオンオブジェクトに固有の識別子がある場合、MAPI は、ログオンオブジェクトにルーティングするすべての要求がそのオブジェクトによって処理されることを保証できます。 ログオンオブジェクトが**MAPIUID**構造を共有する場合、MAPI は、 **MAPIUID**によって識別される最初のログオンオブジェクトに要求をルーティングします。 ログオンオブジェクトのいずれかがエントリ識別子を処理できないため処理できないという要求を受信した場合は、エラーを返す前に、要求を次のログオンオブジェクトに渡します。
  
## <a name="see-also"></a>関連項目



[サービスプロバイダーログオンの実装](implementing-service-provider-logon.md)

