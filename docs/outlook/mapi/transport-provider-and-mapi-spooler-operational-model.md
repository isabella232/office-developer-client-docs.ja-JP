---
title: トランスポート プロバイダーと MAPI スプーラー運用モデル
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b0f8d8f0-fed7-4a7c-bc40-e935f159591d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 5987111844f087801c63989b905992900ff6909c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426626"
---
# <a name="transport-provider-and-mapi-spooler-operational-model"></a><span data-ttu-id="63ddc-103">トランスポート プロバイダーと MAPI スプーラー運用モデル</span><span class="sxs-lookup"><span data-stu-id="63ddc-103">Transport Provider and MAPI Spooler Operational Model</span></span>

  
  
<span data-ttu-id="63ddc-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="63ddc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="63ddc-105">トランスポート プロバイダーの初期化、起動、処理、シャットダウン、および初期化解除は、MAPI スプーラーからトランスポート プロバイダーへの一連の呼び出しによって実行されます。</span><span class="sxs-lookup"><span data-stu-id="63ddc-105">Transport provider initialization, startup, processing, shutdown and deinitialization are accomplished by a series of calls from the MAPI spooler to the transport provider.</span></span> <span data-ttu-id="63ddc-106">呼び出しは次のように順序付けされます。</span><span class="sxs-lookup"><span data-stu-id="63ddc-106">The calls are sequenced as follows:</span></span>
  
1. <span data-ttu-id="63ddc-107">MAPI スプーラーは [、XPProviderInit](xpproviderinit.md) 関数を呼び出し、サポート オブジェクトを渡し、プロバイダー オブジェクトを取得し、トランスポート プロバイダーと MAPI スプーラーが互換性のある MAPI バージョン番号の範囲をサポートしているのを確認します。</span><span class="sxs-lookup"><span data-stu-id="63ddc-107">The MAPI spooler calls the [XPProviderInit](xpproviderinit.md) function, passes a support object, gets the provider object, and checks that the transport provider and MAPI spooler support a compatible range of MAPI version numbers.</span></span> 
    
2. <span data-ttu-id="63ddc-108">MAPI スプーラーは、IXPProvider: IUnknown インターフェイスの [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) メソッド [を呼び出](ixpprovideriunknown.md) します。</span><span class="sxs-lookup"><span data-stu-id="63ddc-108">The MAPI spooler calls the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method of the [IXPProvider : IUnknown](ixpprovideriunknown.md) interface.</span></span> <span data-ttu-id="63ddc-109">MAPI スプーラーとトランスポート プロバイダーの間で、プロファイルの現在のセクションの資格情報を使用してセッションが確立されます。</span><span class="sxs-lookup"><span data-stu-id="63ddc-109">A session is established between the MAPI spooler and the transport provider with the credentials in the current section of the profile.</span></span> <span data-ttu-id="63ddc-110">トランスポート プロバイダーは、ログオン オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="63ddc-110">The transport provider returns a logon object.</span></span> 
    
3. <span data-ttu-id="63ddc-111">MAPI スプーラーは [、IXPLogon::AddressTypes メソッドを呼び出](ixplogon-addresstypes.md) します。</span><span class="sxs-lookup"><span data-stu-id="63ddc-111">The MAPI spooler calls the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> <span data-ttu-id="63ddc-112">トランスポート プロバイダーは、受け入れる一意の識別子 (UID) と電子メール アドレスの種類の一覧を返します。</span><span class="sxs-lookup"><span data-stu-id="63ddc-112">The transport provider returns a list of the unique identifiers (UIDs) and email address types it will accept.</span></span> 
    
4. <span data-ttu-id="63ddc-113">トランスポート プロバイダーは [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) メソッドを呼び出して、MAPI 状態テーブルに行を作成します。</span><span class="sxs-lookup"><span data-stu-id="63ddc-113">The transport provider calls the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method to create its row in the MAPI status table.</span></span> 
    
5. <span data-ttu-id="63ddc-114">MAPI スプーラーは [、IXPLogon::TransportNotify](ixplogon-transportnotify.md) メソッドを呼び出して、メッセージの送受信を有効にします。</span><span class="sxs-lookup"><span data-stu-id="63ddc-114">The MAPI spooler calls the [IXPLogon::TransportNotify](ixplogon-transportnotify.md) method to enable message transmission and reception.</span></span> 
    
6. <span data-ttu-id="63ddc-115">**TransportLogon** 呼び出しの戻り値としてトランスポート プロバイダーから要求された場合、MAPI スプーラーは定期的に [IXPLogon::Idle メソッドを呼び出](ixplogon-idle.md)します。</span><span class="sxs-lookup"><span data-stu-id="63ddc-115">If requested by the transport provider in its return for the **TransportLogon** call, the MAPI spooler periodically calls the [IXPLogon::Idle](ixplogon-idle.md) method.</span></span> <span data-ttu-id="63ddc-116">アイドル処理は、トランスポート プロバイダーが基になるメッセージング システムに新しいメッセージをポーリングする必要がある場合、または他の優先度の低いタスクを実行する必要がある場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="63ddc-116">Idle processing is useful if the transport provider needs to poll the underlying messaging system for new messages or perform other low-priority tasks.</span></span> 
    
7. <span data-ttu-id="63ddc-117">MAPI スプーラーとトランスポート プロバイダーは、メッセージの送受信を行います。</span><span class="sxs-lookup"><span data-stu-id="63ddc-117">The MAPI spooler and transport provider send and receive messages.</span></span> <span data-ttu-id="63ddc-118">詳細については、「Message [Submission Model and Message Reception](message-submission-model.md) [Model」を参照してください](message-reception-model.md)。</span><span class="sxs-lookup"><span data-stu-id="63ddc-118">For more information, see [Message Submission Model](message-submission-model.md) and [Message Reception Model](message-reception-model.md).</span></span> <span data-ttu-id="63ddc-119">MAPI スプーラー は、サポート、メッセージ、および添付ファイル オブジェクトの要求と呼び出しを転送します。</span><span class="sxs-lookup"><span data-stu-id="63ddc-119">The MAPI spooler services transport requests and calls on support, message, and attachment objects.</span></span>
    
8. <span data-ttu-id="63ddc-120">MAPI スプーラーは **、TransportNotify** メソッドを呼び出して、メッセージの送受信を無効にします。</span><span class="sxs-lookup"><span data-stu-id="63ddc-120">The MAPI spooler calls the **TransportNotify** method to disable message transmission and reception.</span></span> 
    
9. <span data-ttu-id="63ddc-121">MAPI スプーラーは、ログオン オブジェクトとプロバイダー オブジェクトを解放します。</span><span class="sxs-lookup"><span data-stu-id="63ddc-121">The MAPI spooler releases the logon and provider objects.</span></span> <span data-ttu-id="63ddc-122">詳細については [、「IXPProvider::Shutdown メソッド」を参照](ixpprovider-shutdown.md) してください。</span><span class="sxs-lookup"><span data-stu-id="63ddc-122">For more information, see the [IXPProvider::Shutdown](ixpprovider-shutdown.md) method.</span></span> 
    

