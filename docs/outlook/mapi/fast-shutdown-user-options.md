---
title: 高速シャット ダウンのユーザー オプション
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 220aeab5-20f6-4520-96c9-8aaa0e8ea15b
description: '最終更新日: 2012 年 6 月 26 日'
ms.openlocfilehash: bd541ed09bc661f3697408d3f475928b9ef0bcc1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585193"
---
# <a name="fast-shutdown-user-options"></a>高速シャット ダウンのユーザー オプション

**適用されます**: Outlook 2013 |Outlook 2016 
  
このトピックでは、3 つ Windows レジストリ設定、使用可能な Microsoft Outlook 2010 で起動して、Microsoft Outlook 2013 では、ユーザーの MAPI クライアントの高速シャット ダウンを含むについて説明します。 管理者は、クライアントの高速シャット ダウンの MAPI プロバイダーのサポートによって優先するクライアントのシャット ダウン動作を指定するのにこれらのレジストリ設定を使用できます。 管理者の設定には、MAPI サブシステムが高速シャット ダウンの利用可能なサポートの観点から[IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md)の MAPI クライアントの呼び出しに応答する方法を決定します。 
  
MAPI クライアントの開発者が、クライアントがその他の MAPI クライアントとは別に高速シャット ダウンをサポートしているかどうかを決定できる場合でも、レジストリの設定では、すべての MAPI クライアントの高速シャット ダウンのユーザー レベルでの管理者の設定を反映と管理者のレジストリ設定です。 とはいえ、正常に実行するのには高速シャット ダウンのユーザーは、必要なレジストリ設定を持つ必要があります、MAPI クライアントを使用して、高速シャット ダウンを開始する必要があります、 [IMAPIClientShutdown: IUnknown](imapiclientshutdowniunknown.md)インターフェイス、および MAPI プロバイダーと連携する、クライアントを実装する必要があります、 [IMAPIProviderShutdown: IUnknown](imapiprovidershutdowniunknown.md)クライアントの高速シャット ダウンをサポートするインターフェイス。 
  
次の一覧では、ユーザー レベルの 3 つのオプションについて説明します。
  
### <a name="option-1-the-mapi-subsystem-enables-fast-shutdown-unless-mapi-providers-explicitly-opt-out"></a>オプション 1: MAPI のサブシステムにより、高速シャット ダウン MAPI プロバイダーが明示的に選択しない限り、 
    
開始すると、Outlook 2010 では、これは、Outlook が MAPI クライアントの場合それは必ずしも他の MAPI クライアントの既定の動作ではありません。 Outlook でこのオプションを明示的に指定するには、管理者は、次のレジストリ キーと値を設定するのには選択できます。
    
レジストリ キー:
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
値:
  
>  `"FastShutdownBehavior"=dword:00000000`
    
返すことによって、MAPI サブシステムがクエリに応答の MAPI クライアントでは、高速シャット ダウンを開始し、高速シャット ダウンをサポートするため、クエリするために**IMAPIClientShutdown::QueryFastShutdown**を呼び出す、ときに S\_限り、アクティブな MAPI いる MAPI プロバイダーがありません [ok]MAPI クライアントとのセッションが高速シャット ダウンのサポートを選択して明示的にします。 

MAPI プロバイダーがエラーを返す[IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md)メソッドを実装することにより高速シャット ダウンを選んだ (MAPI\_E\_NO\_のサポート)。 MAPI サブシステムが MAPI_\E_\NO を返す場合は 1 つまたは複数の MAPI プロバイダーは、 **IMAPIProviderShutdown::QueryFastShutdown**でエラーを返す、\_ **IMAPIClientShutdown::QueryFastShutdown**をサポートします。 

MAPI プロバイダーが、MAPI のサブシステムを返します S を選んだ場合を除き、\_確かに、1 つまたは複数のプロバイダーを実装していない場合でも、 **IMAPIProviderShutdown: IUnknown**インタ フェースです。 
    
### <a name="option-2-the-mapi-subsystem-enables-fast-shutdown-only-if-every-mapi-provider-explicitly-opts-in"></a>オプション 2: MAPI のサブシステムにより、高速シャット ダウンのすべての MAPI プロバイダーが明示的に選んだ場合にのみ 
    
管理者は、次のレジストリ キーおよびクライアントの高速シャット ダウンの環境設定を指定する値を明示的に設定する必要があります。
    
レジストリ キー:
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
値:
  
>  `"FastShutdownBehavior"=dword:00000001`
    
返すことによって、MAPI サブシステムがクエリに応答の MAPI クライアントでは、高速シャット ダウンを開始し、高速シャット ダウンをサポートするため、クエリするために**IMAPIClientShutdown::QueryFastShutdown**を呼び出す、ときに S\_すべての MAPI プロバイダーがアクティブなセッションがある場合に [ok]MAPI クライアント サポート高速シャット ダウンします。 MAPI プロバイダーがエラーのないコードを返すには、 **IMAPIProviderShutdown::QueryFastShutdown**を実装することでのサポートを示します (S\_[ok])。 

このような MAPI プロバイダーが 1 つまたは複数が MAPI を返す場合は、\_E\_NO\_のサポート、または**IMAPIProviderShutdown::QueryFastShutdown**を実装していない MAPI サブシステムは、 **IMAPIClientShutdown::QueryFastShutdown**にエラー コードを返します.
    
### <a name="option-3-an-administrator-disables-support-for-client-fast-shutdown"></a>オプション 3: 管理者はクライアントの高速シャット ダウンのサポートを無効にします
    
管理者は、次のレジストリ キーと値をクライアントの高速シャット ダウンのサポートを無効にするを明示的に設定する必要があります。
    
レジストリ キー:
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
値:
  
>  `"FastShutdownBehavior"=dword:00000002`
    
かどうかに関係なく、MAPI_E_NO_SUPPORT を返すことによって、MAPI サブシステムがクエリに応答と、MAPI クライアントは、高速シャット ダウンを開始し、クエリを高速シャット ダウンをサポートするため**IMAPIClientShutdown::QueryFastShutdown**を呼び出して、任意の MAPI プロバイダーサポートには、シャット ダウンが高速です。 このレジストリ設定は、[MAPI サブシステムは決して任意のプロバイダーの**IMAPIProviderShutdown::QueryFastShutdown**または[IMAPIProviderShutdown::DoFastShutdown](imapiprovidershutdown-dofastshutdown.md)メソッドを呼び出します。 
    
## <a name="see-also"></a>関連項目

- [Mapi クライアントのシャット ダウン](client-shutdown-in-mapi.md)
- [高速シャットダウンの概要](fast-shutdown-overview.md)
- [高速シャットダウンのためのベスト プラクティス](best-practices-for-fast-shutdown.md)

