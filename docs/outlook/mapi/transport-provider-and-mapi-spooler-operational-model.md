---
title: トランスポート プロバイダーと MAPI スプーラー運用モデル
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b0f8d8f0-fed7-4a7c-bc40-e935f159591d
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 0e6c38091e5b2e10e82012bc470ea41037f57c7d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804138"
---
# <a name="transport-provider-and-mapi-spooler-operational-model"></a><span data-ttu-id="6e56e-103">トランスポート プロバイダーと MAPI スプーラー運用モデル</span><span class="sxs-lookup"><span data-stu-id="6e56e-103">Transport Provider and MAPI Spooler Operational Model</span></span>

  
  
<span data-ttu-id="6e56e-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6e56e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6e56e-105">トランスポート プロバイダーの初期化、起動、処理、シャット ダウン、二つの後処理は、一連の MAPI スプーラーからトランスポート プロバイダーへの呼び出しによって実行されます。</span><span class="sxs-lookup"><span data-stu-id="6e56e-105">Transport provider initialization, startup, processing, shutdown and deinitialization are accomplished by a series of calls from the MAPI spooler to the transport provider.</span></span> <span data-ttu-id="6e56e-106">呼び出しは次のように順序付けられました。</span><span class="sxs-lookup"><span data-stu-id="6e56e-106">The calls are sequenced as follows:</span></span>
  
1. <span data-ttu-id="6e56e-107">MAPI スプーラー [XPProviderInit](xpproviderinit.md)関数を呼び出し、オブジェクトがサポート、プロバイダー オブジェクトを取得、トランスポート プロバイダーが、MAPI スプーラーが互換性のある範囲の MAPI のバージョン番号をサポートすることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6e56e-107">The MAPI spooler calls the [XPProviderInit](xpproviderinit.md) function, passes a support object, gets the provider object, and checks that the transport provider and MAPI spooler support a compatible range of MAPI version numbers.</span></span> 
    
2. <span data-ttu-id="6e56e-108">MAPI スプーラーは、の[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)メソッドを呼び出して、 [IXPProvider: IUnknown](ixpprovideriunknown.md)インタ フェースです。</span><span class="sxs-lookup"><span data-stu-id="6e56e-108">The MAPI spooler calls the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method of the [IXPProvider : IUnknown](ixpprovideriunknown.md) interface.</span></span> <span data-ttu-id="6e56e-109">MAPI スプーラーとプロファイルの現在のセクション内の資格情報を使用してトランスポート プロバイダーの間でセッションが確立されます。</span><span class="sxs-lookup"><span data-stu-id="6e56e-109">A session is established between the MAPI spooler and the transport provider with the credentials in the current section of the profile.</span></span> <span data-ttu-id="6e56e-110">トランスポート プロバイダーでは、ログオン オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="6e56e-110">The transport provider returns a logon object.</span></span> 
    
3. <span data-ttu-id="6e56e-111">MAPI スプーラーは、 [IXPLogon::AddressTypes](ixplogon-addresstypes.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6e56e-111">The MAPI spooler calls the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> <span data-ttu-id="6e56e-112">トランスポート プロバイダーは、受け入れることは、一意識別子 (Uid) と電子メール アドレスの種類の一覧を返します。</span><span class="sxs-lookup"><span data-stu-id="6e56e-112">The transport provider returns a list of the unique identifiers (UIDs) and email address types it will accept.</span></span> 
    
4. <span data-ttu-id="6e56e-113">トランスポート プロバイダーでは、MAPI の状態テーブル内の行を作成する[IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6e56e-113">The transport provider calls the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method to create its row in the MAPI status table.</span></span> 
    
5. <span data-ttu-id="6e56e-114">MAPI スプーラーでは、メッセージの送信と受信を有効にする[IXPLogon::TransportNotify](ixplogon-transportnotify.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6e56e-114">The MAPI spooler calls the [IXPLogon::TransportNotify](ixplogon-transportnotify.md) method to enable message transmission and reception.</span></span> 
    
6. <span data-ttu-id="6e56e-115">**TransportLogon**呼び出し、その戻り値のトランスポート プロバイダーによって要求されると、MAPI スプーラーは定期的に[IXPLogon::Idle](ixplogon-idle.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6e56e-115">If requested by the transport provider in its return for the **TransportLogon** call, the MAPI spooler periodically calls the [IXPLogon::Idle](ixplogon-idle.md) method.</span></span> <span data-ttu-id="6e56e-116">アイドル処理では、トランスポート プロバイダーが新しいメッセージの基になるメッセージング システムをポーリングまたはその他の優先度の低いタスクを実行する必要がある場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="6e56e-116">Idle processing is useful if the transport provider needs to poll the underlying messaging system for new messages or perform other low-priority tasks.</span></span> 
    
7. <span data-ttu-id="6e56e-117">MAPI スプーラーとトランスポート プロバイダー メッセージを送信します。</span><span class="sxs-lookup"><span data-stu-id="6e56e-117">The MAPI spooler and transport provider send and receive messages.</span></span> <span data-ttu-id="6e56e-118">詳細については、[メッセージの送信のモデル](message-submission-model.md)と[メッセージの受信のモデル](message-reception-model.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6e56e-118">For more information, see [Message Submission Model](message-submission-model.md) and [Message Reception Model](message-reception-model.md).</span></span> <span data-ttu-id="6e56e-119">MAPI スプーラーは、トランスポートの要求を処理し、サポート、メッセージ、および添付ファイルのオブジェクトを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6e56e-119">The MAPI spooler services transport requests and calls on support, message, and attachment objects.</span></span>
    
8. <span data-ttu-id="6e56e-120">MAPI スプーラーでは、メッセージの送受信を無効にする**TransportNotify**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6e56e-120">The MAPI spooler calls the **TransportNotify** method to disable message transmission and reception.</span></span> 
    
9. <span data-ttu-id="6e56e-121">MAPI スプーラーは、ログオン、およびプロバイダーのオブジェクトを解放します。</span><span class="sxs-lookup"><span data-stu-id="6e56e-121">The MAPI spooler releases the logon and provider objects.</span></span> <span data-ttu-id="6e56e-122">詳細については、 [IXPProvider::Shutdown](ixpprovider-shutdown.md)メソッドを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6e56e-122">For more information, see the [IXPProvider::Shutdown](ixpprovider-shutdown.md) method.</span></span> 
    

