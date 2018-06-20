---
title: トランスポート プロバイダーを解放します。
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e0f37485-55c9-40f0-bc8c-48f7297f9f50
description: '�ŏI�X�V��: 2015�N12��7��'
ms.openlocfilehash: b8032b22c78ae34bce7e9ccfb0f0a14cdde07290
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803739"
---
# <a name="releasing-the-transport-provider"></a><span data-ttu-id="d43e9-103">トランスポート プロバイダーを解放します。</span><span class="sxs-lookup"><span data-stu-id="d43e9-103">Releasing the Transport Provider</span></span>

 
  
<span data-ttu-id="d43e9-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d43e9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d43e9-105">MAPI、または MAPI スプーラーが終了したときトランスポート ログオン オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="d43e9-105">When MAPI or the MAPI spooler finishes using a transport logon object:</span></span>
  
1. <span data-ttu-id="d43e9-106">MAPI、または MAPI スプーラーは、トランスポート プロバイダーの[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d43e9-106">MAPI or the MAPI spooler calls the transport provider's [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) method.</span></span> 
    
2. <span data-ttu-id="d43e9-107">トランスポート プロバイダーは、 [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md)メソッドを呼び出して、状態オブジェクトを無効にします。</span><span class="sxs-lookup"><span data-stu-id="d43e9-107">The transport provider invalidates the status object by calling the [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) method.</span></span> <span data-ttu-id="d43e9-108">トランスポート プロバイダーは、メッセージ オブジェクトを無効にするかどうか送信または**TransportLogoff**の呼び出し時に受信されるが**TransportLogoff**に渡されたフラグに依存します。</span><span class="sxs-lookup"><span data-stu-id="d43e9-108">Whether the transport provider invalidates message objects that are being sent or received at the time of the **TransportLogoff** call depends on the flags that were passed to **TransportLogoff**.</span></span>
    
3. <span data-ttu-id="d43e9-109">トランスポート プロバイダーは、状態テーブルから、トランスポート プロバイダーの行を削除して、一意の識別子 (Uid) [IMAPISupport で設定された内部テーブルからを削除するサポート オブジェクトの[リ ス](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx)のメソッドを呼び出して、:。SetProviderUID](imapisupport-setprovideruid.md)メソッドです。</span><span class="sxs-lookup"><span data-stu-id="d43e9-109">The transport provider calls the support object's [IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method to remove the transport provider's row from the status table and remove from internal tables any unique identifiers (UIDs) that were set with the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method.</span></span> <span data-ttu-id="d43e9-110">それをデクリメントこのプロバイダー オブジェクトのアクティブなログオンが正常のオブジェクトの数です。</span><span class="sxs-lookup"><span data-stu-id="d43e9-110">It decrements the count of known logon objects active on this provider object.</span></span> <span data-ttu-id="d43e9-111">カウントが 0 になった場合、MAPI はプロバイダー オブジェクトの**リリース**、 [IXPProvider::Shutdown](ixpprovider-shutdown.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d43e9-111">If the count reaches zero, MAPI calls the [IXPProvider::Shutdown](ixpprovider-shutdown.md) method and **Release** on the provider object.</span></span> <span data-ttu-id="d43e9-112">最後の既知のプロバイダー オブジェクトがこのプロセスでこの DLL を使用する場合、MAPI は、後で、DLL の**終わった**関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d43e9-112">If this was the last known provider object using this DLL on this process, MAPI calls the **FreeLibrary** function on the DLL at a later time.</span></span> <span data-ttu-id="d43e9-113">MAPI サポート オブジェクトのメモリは解放され、 **Release**メソッドのサポート オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="d43e9-113">Memory for the MAPI support object is freed and the support object **Release** method returns.</span></span> 
    
4. <span data-ttu-id="d43e9-114">**TransportLogoff**メソッドは S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="d43e9-114">The **TransportLogoff** method returns S_OK.</span></span> 
    
5. <span data-ttu-id="d43e9-115">MAPI、または MAPI スプーラーは、トランスポート プロバイダーのログオン オブジェクトの**リリース**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d43e9-115">MAPI or the MAPI spooler calls **Release** on the transport provider's logon object.</span></span> <span data-ttu-id="d43e9-116">オブジェクトのメモリを解放するとします。</span><span class="sxs-lookup"><span data-stu-id="d43e9-116">The memory for the object is released.</span></span> 
    
6. <span data-ttu-id="d43e9-117">MAPI、または MAPI スプーラーは、プロバイダーの DLL に**終わった**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d43e9-117">MAPI or the MAPI spooler calls **FreeLibrary** on the provider DLL.</span></span> 
    
<span data-ttu-id="d43e9-118">堅牢性、ログオンし、プロバイダーのオブジェクトは、 **TransportLogoff**または**シャット ダウン**の方法と呼ばれることがなく自身の最終の**解放**呼び出しを処理することにあります。</span><span class="sxs-lookup"><span data-stu-id="d43e9-118">For robustness, the logon and provider objects should be able to handle final **Release** calls on themselves without first having their **TransportLogoff** or **Shutdown** methods called.</span></span> <span data-ttu-id="d43e9-119">**リリース**はこのような場合に呼び出されると、トランスポート プロバイダーは、 **TransportLogoff**または**シャット ダウン****のリリース**の後に 0 個の引数を指定して呼び出された場合と同様に呼び出しを扱う必要があります。</span><span class="sxs-lookup"><span data-stu-id="d43e9-119">If **Release** is called in such cases, transport providers should treat the calls as if **TransportLogoff** or **Shutdown** had been called with a zero argument followed by **Release**.</span></span>
  

