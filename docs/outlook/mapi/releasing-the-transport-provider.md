---
title: トランスポート プロバイダーの解放
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
# <a name="releasing-the-transport-provider"></a><span data-ttu-id="b1fd7-103">トランスポート プロバイダーの解放</span><span class="sxs-lookup"><span data-stu-id="b1fd7-103">Releasing the Transport Provider</span></span>

 
  
<span data-ttu-id="b1fd7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1fd7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b1fd7-105">MAPI または MAPI スプーラーがトランスポート ログオン オブジェクトの使用を終了すると、次の処理が完了します。</span><span class="sxs-lookup"><span data-stu-id="b1fd7-105">When MAPI or the MAPI spooler finishes using a transport logon object:</span></span>
  
1. <span data-ttu-id="b1fd7-106">MAPI または MAPI スプーラーは、トランスポート プロバイダーの [IXPLogon::TransportLogoff メソッドを呼び出](ixplogon-transportlogoff.md) します。</span><span class="sxs-lookup"><span data-stu-id="b1fd7-106">MAPI or the MAPI spooler calls the transport provider's [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) method.</span></span> 
    
2. <span data-ttu-id="b1fd7-107">トランスポート プロバイダーは [、IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) メソッドを呼び出して、status オブジェクトを無効にします。</span><span class="sxs-lookup"><span data-stu-id="b1fd7-107">The transport provider invalidates the status object by calling the [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) method.</span></span> <span data-ttu-id="b1fd7-108">トランスポート プロバイダーが **TransportLogoff** 呼び出し時に送信または受信されるメッセージ オブジェクトを無効にするかどうかは **、TransportLogoff** に渡されたフラグによって異なります。</span><span class="sxs-lookup"><span data-stu-id="b1fd7-108">Whether the transport provider invalidates message objects that are being sent or received at the time of the **TransportLogoff** call depends on the flags that were passed to **TransportLogoff**.</span></span>
    
3. <span data-ttu-id="b1fd7-109">トランスポート プロバイダーは、サポート オブジェクトの [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) メソッドを呼び出して、トランスポート プロバイダーの行を状態テーブルから削除し [、IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) メソッドで設定された一意の識別子 (UID) を内部テーブルから削除します。</span><span class="sxs-lookup"><span data-stu-id="b1fd7-109">The transport provider calls the support object's [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method to remove the transport provider's row from the status table and remove from internal tables any unique identifiers (UIDs) that were set with the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method.</span></span> <span data-ttu-id="b1fd7-110">このプロバイダー オブジェクトでアクティブな既知のログオン オブジェクトの数をデクレメントします。</span><span class="sxs-lookup"><span data-stu-id="b1fd7-110">It decrements the count of known logon objects active on this provider object.</span></span> <span data-ttu-id="b1fd7-111">カウントが 0 に達すると、MAPI は [IXPProvider::Shutdown](ixpprovider-shutdown.md) メソッドと **Release** をプロバイダー オブジェクトで呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b1fd7-111">If the count reaches zero, MAPI calls the [IXPProvider::Shutdown](ixpprovider-shutdown.md) method and **Release** on the provider object.</span></span> <span data-ttu-id="b1fd7-112">このプロセスでこの DLL を使用する最後の既知のプロバイダー オブジェクトである場合、MAPI は後で DLL の **FreeLibrary** 関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b1fd7-112">If this was the last known provider object using this DLL on this process, MAPI calls the **FreeLibrary** function on the DLL at a later time.</span></span> <span data-ttu-id="b1fd7-113">MAPI サポート オブジェクトのメモリが解放され、サポート オブジェクト **Release** メソッドが返されます。</span><span class="sxs-lookup"><span data-stu-id="b1fd7-113">Memory for the MAPI support object is freed and the support object **Release** method returns.</span></span> 
    
4. <span data-ttu-id="b1fd7-114">**TransportLogoff メソッドは**、次のS_OK。</span><span class="sxs-lookup"><span data-stu-id="b1fd7-114">The **TransportLogoff** method returns S_OK.</span></span> 
    
5. <span data-ttu-id="b1fd7-115">MAPI または MAPI スプーラーは、トランスポート **プロバイダー** のログオン オブジェクトで Release を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b1fd7-115">MAPI or the MAPI spooler calls **Release** on the transport provider's logon object.</span></span> <span data-ttu-id="b1fd7-116">オブジェクトのメモリが解放されます。</span><span class="sxs-lookup"><span data-stu-id="b1fd7-116">The memory for the object is released.</span></span> 
    
6. <span data-ttu-id="b1fd7-117">MAPI または MAPI スプーラーは、プロバイダー DLL **で FreeLibrary** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b1fd7-117">MAPI or the MAPI spooler calls **FreeLibrary** on the provider DLL.</span></span> 
    
<span data-ttu-id="b1fd7-118">堅牢性を高めるには、ログオン オブジェクトとプロバイダー オブジェクトは、最初に **TransportLogoff** メソッドまたは **Shutdown** メソッドを呼び出さずに、自身で最終的なリリース呼び出しを処理できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1fd7-118">For robustness, the logon and provider objects should be able to handle final **Release** calls on themselves without first having their **TransportLogoff** or **Shutdown** methods called.</span></span> <span data-ttu-id="b1fd7-119">このような **場合に** Release が呼び出された場合、トランスポート プロバイダーは、引数が 0 の **TransportLogoff** または **Shutdown** が呼び出された場合と同様に呼び出しを処理し、その後に Release を指定 **します**。</span><span class="sxs-lookup"><span data-stu-id="b1fd7-119">If **Release** is called in such cases, transport providers should treat the calls as if **TransportLogoff** or **Shutdown** had been called with a zero argument followed by **Release**.</span></span>
  

