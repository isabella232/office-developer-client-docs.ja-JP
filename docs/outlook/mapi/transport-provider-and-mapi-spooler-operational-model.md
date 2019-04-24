---
title: トランスポートプロバイダーと MAPI スプーラー運用モデル
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b0f8d8f0-fed7-4a7c-bc40-e935f159591d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 5987111844f087801c63989b905992900ff6909c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356610"
---
# <a name="transport-provider-and-mapi-spooler-operational-model"></a><span data-ttu-id="07808-103">トランスポートプロバイダーと MAPI スプーラー運用モデル</span><span class="sxs-lookup"><span data-stu-id="07808-103">Transport Provider and MAPI Spooler Operational Model</span></span>

  
  
<span data-ttu-id="07808-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="07808-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="07808-105">トランスポートプロバイダーの初期化、スタートアップ、処理、シャットダウン、および deinitialization は、MAPI スプーラーからトランスポートプロバイダーへの一連の呼び出しによって実行されます。</span><span class="sxs-lookup"><span data-stu-id="07808-105">Transport provider initialization, startup, processing, shutdown and deinitialization are accomplished by a series of calls from the MAPI spooler to the transport provider.</span></span> <span data-ttu-id="07808-106">呼び出しは次のように順序付けられます。</span><span class="sxs-lookup"><span data-stu-id="07808-106">The calls are sequenced as follows:</span></span>
  
1. <span data-ttu-id="07808-107">mapi スプーラーは、 [xps の init](xpproviderinit.md)関数を呼び出し、サポートオブジェクトを渡して、プロバイダーオブジェクトを取得します。また、トランスポートプロバイダーと mapi スプーラーが、互換性のある mapi バージョン番号の範囲をサポートしているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="07808-107">The MAPI spooler calls the [XPProviderInit](xpproviderinit.md) function, passes a support object, gets the provider object, and checks that the transport provider and MAPI spooler support a compatible range of MAPI version numbers.</span></span> 
    
2. <span data-ttu-id="07808-108">MAPI スプーラーは、 [ixpprovider: IUnknown](ixpprovideriunknown.md)インターフェイスの[ixpprovider:: transportlogon](ixpprovider-transportlogon.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="07808-108">The MAPI spooler calls the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method of the [IXPProvider : IUnknown](ixpprovideriunknown.md) interface.</span></span> <span data-ttu-id="07808-109">プロファイルの現在のセクションの資格情報を使用して、MAPI スプーラーとトランスポートプロバイダーの間にセッションが確立されます。</span><span class="sxs-lookup"><span data-stu-id="07808-109">A session is established between the MAPI spooler and the transport provider with the credentials in the current section of the profile.</span></span> <span data-ttu-id="07808-110">トランスポートプロバイダーがログオンオブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="07808-110">The transport provider returns a logon object.</span></span> 
    
3. <span data-ttu-id="07808-111">MAPI スプーラーは、 [IXPLogon:: AddressTypes](ixplogon-addresstypes.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="07808-111">The MAPI spooler calls the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> <span data-ttu-id="07808-112">トランスポートプロバイダーは、受け付ける一意識別子 (uid) と電子メールアドレスの種類の一覧を返します。</span><span class="sxs-lookup"><span data-stu-id="07808-112">The transport provider returns a list of the unique identifiers (UIDs) and email address types it will accept.</span></span> 
    
4. <span data-ttu-id="07808-113">トランスポートプロバイダーは、MAPI 状態テーブルに行を作成する[imapisupport:: modifystatusrow](imapisupport-modifystatusrow.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="07808-113">The transport provider calls the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method to create its row in the MAPI status table.</span></span> 
    
5. <span data-ttu-id="07808-114">MAPI スプーラーは、 [IXPLogon:: transportnotify](ixplogon-transportnotify.md)メソッドを呼び出して、メッセージの送信と受信を有効にします。</span><span class="sxs-lookup"><span data-stu-id="07808-114">The MAPI spooler calls the [IXPLogon::TransportNotify](ixplogon-transportnotify.md) method to enable message transmission and reception.</span></span> 
    
6. <span data-ttu-id="07808-115">トランスポートプロバイダーによって、 **transportlogon**呼び出しに対して戻り値が要求されると、MAPI スプーラーは[IXPLogon:: Idle](ixplogon-idle.md)メソッドを定期的に呼び出します。</span><span class="sxs-lookup"><span data-stu-id="07808-115">If requested by the transport provider in its return for the **TransportLogon** call, the MAPI spooler periodically calls the [IXPLogon::Idle](ixplogon-idle.md) method.</span></span> <span data-ttu-id="07808-116">アイドル処理は、トランスポートプロバイダーが、新しいメッセージの基礎となるメッセージングシステムをポーリングしたり、優先度の低いタスクを実行したりする必要がある場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="07808-116">Idle processing is useful if the transport provider needs to poll the underlying messaging system for new messages or perform other low-priority tasks.</span></span> 
    
7. <span data-ttu-id="07808-117">MAPI スプーラーとトランスポートプロバイダーは、メッセージを送受信します。</span><span class="sxs-lookup"><span data-stu-id="07808-117">The MAPI spooler and transport provider send and receive messages.</span></span> <span data-ttu-id="07808-118">詳細については、「[メッセージ送信モデル](message-submission-model.md)および[メッセージ受信モデル](message-reception-model.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="07808-118">For more information, see [Message Submission Model](message-submission-model.md) and [Message Reception Model](message-reception-model.md).</span></span> <span data-ttu-id="07808-119">MAPI スプーラーサービスは、サポート、メッセージ、および添付ファイルオブジェクトのトランスポート要求と呼び出しを行います。</span><span class="sxs-lookup"><span data-stu-id="07808-119">The MAPI spooler services transport requests and calls on support, message, and attachment objects.</span></span>
    
8. <span data-ttu-id="07808-120">MAPI スプーラーは、メッセージの送信と受信を無効にするために、 **transportnotify**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="07808-120">The MAPI spooler calls the **TransportNotify** method to disable message transmission and reception.</span></span> 
    
9. <span data-ttu-id="07808-121">MAPI スプーラーは、ログオンおよびプロバイダーオブジェクトを解放します。</span><span class="sxs-lookup"><span data-stu-id="07808-121">The MAPI spooler releases the logon and provider objects.</span></span> <span data-ttu-id="07808-122">詳細については、 [ixpprovider:: Shutdown](ixpprovider-shutdown.md)メソッドを参照してください。</span><span class="sxs-lookup"><span data-stu-id="07808-122">For more information, see the [IXPProvider::Shutdown](ixpprovider-shutdown.md) method.</span></span> 
    

