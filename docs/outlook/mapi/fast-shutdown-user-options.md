---
title: 高速シャットダウンのユーザー オプション
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
api_type:
- COM
ms.assetid: 220aeab5-20f6-4520-96c9-8aaa0e8ea15b
description: '最終更新日: 2012 年 6 月 26 日'
localization_priority: Priority
ms.openlocfilehash: 3c60862733c6b38e60650ae9daba9bba578fcd58
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341077"
---
# <a name="fast-shutdown-user-options"></a>高速シャットダウンのユーザー オプション

**適用対象**: Outlook 2013 | Outlook 2016 
  
このトピックでは、ユーザーの MAPI クライアントを高速シャットダウンするための 3 つの Windows レジストリ設定について説明します。この設定は、この設定は、Microsoft Outlook 2010 から現在の Microsoft Outlook 2013 で使用できます。 この 3 つのレジストリ設定を使用することで、管理者はクライアントの高速シャットダウンに対する MAPI プロバイダーのサポートに応じて優先されるクライアント シャットダウン動作を指定できます。 管理者の設定により、MAPI サブシステムが [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) に対する MAPI クライアントの呼び出しに利用可能な高速シャットダウンのサポートに関して応答する方法が決まります。 
  
レジストリ設定は、すべての MAPI クライアントの高速シャットダウンに対する管理者の優先設定をユーザー レベルで反映しますが、MAPI クライアントの開発者は、その他の MAPI クライアントの設定および管理者のレジストリ設定とは無関係に、クライアントで高速シャットダウンをサポートするかどうかを決定できます。 ただし、高速シャットダウンを正常に実施するには、ユーザーが必要なレジストリ設定を保持し、MAPI クライアントが [IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md) インターフェイスを使用して高速シャットダウンを開始し、クライアントと連携する MAPI プロバイダーはクライアントの高速シャットダウンをサポートする [IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md) インターフェイスを実装する必要があります。 
  
次に、これら 3 つのユーザー レベルのオプションについて説明します。
  
### <a name="option-1-the-mapi-subsystem-enables-fast-shutdown-unless-mapi-providers-explicitly-opt-out"></a>オプション 1: MAPI サブシステムで高速シャットダウンを有効にする (ただし、MAPI プロバイダーが明示的に無効にしている場合を除く) 
    
Outlook 2010 以降、Outlook が MAPI クライアントのときには、この動作が既定の動作になります。これは、その他の MAPI クライアントの既定の動作ではない場合があります。 このオプションを Outlook に明示的に指定するために、管理者は次のレジストリ キーと値を設定することもできます。
    
レジストリ キー:
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
値:
  
>  `"FastShutdownBehavior"=dword:00000000`
    
MAPI クライアントが高速シャットダウンを開始し、高速シャットダウンのサポートについてクエリするために **IMAPIClientShutdown::QueryFastShutdown** を呼び出すと、MAPI サブシステムは、S\_OK を返すことでクエリに応答します。ただし、MAPI クライアントとのアクティブな MAPI セッションを持つ MAPI プロバイダーが高速シャットダウンのサポートを明示的に無効にしている場合を除きます。 

MAPI プロバイダーは、エラー (MAPI\_E\_NO\_SUPPORT) を返す [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) メソッドを実装することで、高速シャットダウンを無効にします。 1 つ以上の MAPI プロバイダーが **IMAPIProviderShutdown::QueryFastShutdown** でエラーを返すと、MAPI サブシステムは **IMAPIClientShutdown::QueryFastShutdown** に MAPI_\E_\NO\_SUPPORT を返します。 

MAPI プロバイダーが無効にしていない限り、1 つ以上のプロバイダーが **IMAPIProviderShutdown : IUnknown** を実装していない場合でも、MAPI サブシステムは S\_OK を返します。 
    
### <a name="option-2-the-mapi-subsystem-enables-fast-shutdown-only-if-every-mapi-provider-explicitly-opts-in"></a>オプション 2: すべての MAPI プロバイダーが明示的に有効化している場合にのみ MAPI サブシステムで高速シャットダウンを有効にする 
    
管理者は、この優先設定をクライアントの高速シャットダウンに指定するために、次のレジストリ キーと値を明示的に設定する必要があります。
    
レジストリ キー:
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
値:
  
>  `"FastShutdownBehavior"=dword:00000001`
    
MAPI クライアントが高速シャットダウンを開始し、高速シャットダウンのサポートについてクエリするために **IMAPIClientShutdown::QueryFastShutdown** を呼び出すと、MAPI サブシステムは、MAPI クライアントとのアクティブな MAPI セッションを持つすべての MAPI プロバイダーが高速シャットダウンをサポートしている場合に S\_OK を返すことでクエリに応答します。 MAPI プロバイダーは、エラーではないコード (S\_OK) を返す **IMAPIProviderShutdown::QueryFastShutdown** を実装することで、サポートしていることを示します。 

1 つ以上の MAPI プロバイダーが MAPI\_E\_NO\_SUPPORT を返した場合や、**IMAPIProviderShutdown::QueryFastShutdown** を実装していない場合、MAPI サブシステムは **IMAPIClientShutdown::QueryFastShutdown** にエラー コードを返します。
    
### <a name="option-3-an-administrator-disables-support-for-client-fast-shutdown"></a>オプション 3: 管理者がクライアントの高速シャットダウンを無効にする
    
管理者は、クライアントの高速シャットダウンを無効にするために、次のレジストリ キーと値を明示的に設定する必要があります。
    
レジストリ キー:
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
値:
  
>  `"FastShutdownBehavior"=dword:00000002`
    
MAPI クライアントが高速シャットダウンを開始し、高速シャットダウンのサポートについてクエリするために **IMAPIClientShutdown::QueryFastShutdown** を呼び出すと、MAPI サブシステムは、MAPI プロバイダーが高速シャットダウンをサポートしているかどうかに関係なく MAPI_E_NO_SUPPORT を返すことでクエリに応答します。 このレジストリ設定により、MAPI サブシステムはプロバイダーの **IMAPIProviderShutdown::QueryFastShutdown** メソッドまたは [IMAPIProviderShutdown::DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) メソッドを呼び出さなくなります。 
    
## <a name="see-also"></a>関連項目

- [MAPI でのクライアント シャットダウン](client-shutdown-in-mapi.md)
- [高速シャットダウンの概要](fast-shutdown-overview.md)
- [高速シャットダウンのためのベスト プラクティス](best-practices-for-fast-shutdown.md)

