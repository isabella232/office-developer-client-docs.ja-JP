---
title: トランスポートプロバイダーを解放する
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e0f37485-55c9-40f0-bc8c-48f7297f9f50
description: '�ŏI�X�V��: 2015�N12��7��'
ms.openlocfilehash: 41d953db8e00ff52cd09a27e2f7550f9f1879321
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328386"
---
# <a name="releasing-the-transport-provider"></a><span data-ttu-id="74995-103">トランスポートプロバイダーを解放する</span><span class="sxs-lookup"><span data-stu-id="74995-103">Releasing the Transport Provider</span></span>

 
  
<span data-ttu-id="74995-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74995-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74995-105">mapi または mapi スプーラーがトランスポートログオンオブジェクトを使用して終了した場合:</span><span class="sxs-lookup"><span data-stu-id="74995-105">When MAPI or the MAPI spooler finishes using a transport logon object:</span></span>
  
1. <span data-ttu-id="74995-106">mapi または mapi スプーラーは、トランスポートプロバイダーの[IXPLogon:: transportlogoff](ixplogon-transportlogoff.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="74995-106">MAPI or the MAPI spooler calls the transport provider's [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) method.</span></span> 
    
2. <span data-ttu-id="74995-107">トランスポートプロバイダーは、 [imapisupport:: makeinvalid](imapisupport-makeinvalid.md)メソッドを呼び出して、status オブジェクトを無効にします。</span><span class="sxs-lookup"><span data-stu-id="74995-107">The transport provider invalidates the status object by calling the [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) method.</span></span> <span data-ttu-id="74995-108">transport **logoff**呼び出しの時点で送受信されたメッセージオブジェクトがトランスポートプロバイダによって無効にされるかどうかは、 **transportlogoff**に渡されたフラグによって決まります。</span><span class="sxs-lookup"><span data-stu-id="74995-108">Whether the transport provider invalidates message objects that are being sent or received at the time of the **TransportLogoff** call depends on the flags that were passed to **TransportLogoff**.</span></span>
    
3. <span data-ttu-id="74995-109">トランスポートプロバイダーは、サポートオブジェクトの[IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx)メソッドを呼び出して、状態テーブルからトランスポートプロバイダーの行を削除し、imapisupport で設定された一意識別子 (uid) をすべて内部テーブルから削除します。 [setprovideruid](imapisupport-setprovideruid.md)メソッド。</span><span class="sxs-lookup"><span data-stu-id="74995-109">The transport provider calls the support object's [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method to remove the transport provider's row from the status table and remove from internal tables any unique identifiers (UIDs) that were set with the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method.</span></span> <span data-ttu-id="74995-110">このプロバイダーオブジェクトでアクティブになっている既知のログオンオブジェクトの数をデクリメントします。</span><span class="sxs-lookup"><span data-stu-id="74995-110">It decrements the count of known logon objects active on this provider object.</span></span> <span data-ttu-id="74995-111">数が0になると、MAPI は、プロバイダーオブジェクトで[ixpprovider:: Shutdown](ixpprovider-shutdown.md)メソッドと**Release**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="74995-111">If the count reaches zero, MAPI calls the [IXPProvider::Shutdown](ixpprovider-shutdown.md) method and **Release** on the provider object.</span></span> <span data-ttu-id="74995-112">このプロセスでこの dll を使用する最後の既知のプロバイダーオブジェクトである場合、MAPI は dll の**FreeLibrary**関数を後で呼び出します。</span><span class="sxs-lookup"><span data-stu-id="74995-112">If this was the last known provider object using this DLL on this process, MAPI calls the **FreeLibrary** function on the DLL at a later time.</span></span> <span data-ttu-id="74995-113">MAPI サポートオブジェクトのメモリは解放され、support オブジェクトの**Release**メソッドは返されます。</span><span class="sxs-lookup"><span data-stu-id="74995-113">Memory for the MAPI support object is freed and the support object **Release** method returns.</span></span> 
    
4. <span data-ttu-id="74995-114">**transportlogoff**メソッドは S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="74995-114">The **TransportLogoff** method returns S_OK.</span></span> 
    
5. <span data-ttu-id="74995-115">mapi または mapi スプーラーは、トランスポートプロバイダーのログオンオブジェクトで**リリース**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="74995-115">MAPI or the MAPI spooler calls **Release** on the transport provider's logon object.</span></span> <span data-ttu-id="74995-116">オブジェクトのメモリが解放されます。</span><span class="sxs-lookup"><span data-stu-id="74995-116">The memory for the object is released.</span></span> 
    
6. <span data-ttu-id="74995-117">mapi または mapi スプーラーは、プロバイダー DLL で**FreeLibrary**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="74995-117">MAPI or the MAPI spooler calls **FreeLibrary** on the provider DLL.</span></span> 
    
<span data-ttu-id="74995-118">堅牢性を考慮して、ログオンおよびプロバイダーオブジェクトは、最初に**transportlogoff**または**Shutdown**メソッドを呼び出さずに、それ自体の最終**リリース**呼び出しを処理できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="74995-118">For robustness, the logon and provider objects should be able to handle final **Release** calls on themselves without first having their **TransportLogoff** or **Shutdown** methods called.</span></span> <span data-ttu-id="74995-119">このような場合に**release**が呼び出された場合、トランスポートプロバイダーは、 \*\*\*\* 引数ゼロを\*\*\*\* 指定して**release**を呼び出した場合と同様に、呼び出しを処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="74995-119">If **Release** is called in such cases, transport providers should treat the calls as if **TransportLogoff** or **Shutdown** had been called with a zero argument followed by **Release**.</span></span>
  

