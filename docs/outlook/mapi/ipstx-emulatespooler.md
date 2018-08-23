---
title: IPSTXEmulateSpooler
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX.EmulateSpooler
api_type:
- COM
ms.assetid: aec72e51-1f75-b2c5-76ca-626cd21fbc7d
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a8e353bbb4f276169ae26ba9d05821158bf55f00
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801194"
---
# <a name="ipstxemulatespooler"></a><span data-ttu-id="04878-103">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="04878-103">IPSTX::EmulateSpooler</span></span>

  
  
<span data-ttu-id="04878-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="04878-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="04878-105">サーバーに送信するメッセージをスプールする Outlook プロトコル マネージャーをエミュレートするためにローカル ストアを設定します。</span><span class="sxs-lookup"><span data-stu-id="04878-105">Sets a local store to emulate the Outlook Protocol Manager to spool outgoing messages to a server.</span></span>
  
```cpp
HRESULT EmulateSpooler( 
    BOOL fEmulate 
);
```

 <span data-ttu-id="04878-106">_fEmulate_</span><span class="sxs-lookup"><span data-stu-id="04878-106">_fEmulate_</span></span>
  
>  <span data-ttu-id="04878-107">[in]ローカル ストアはスプーラーをエミュレートする必要がある場合、このパラメーターを True に設定します。そうでない場合は、False に設定します。</span><span class="sxs-lookup"><span data-stu-id="04878-107">[in] Set this parameter to True if the local store should emulate the spooler; set it to False if not.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="04878-108">注釈</span><span class="sxs-lookup"><span data-stu-id="04878-108">Remarks</span></span>

<span data-ttu-id="04878-109">ローカル ストアは、Outlook プロトコル マネージャーとして、処理のためのバックエンドのサーバー (たとえば、MSN のサーバーまたは AOL サーバー) に送信キューにメッセージをスプールを動作するように**IPSTX::EmulateSpooler**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="04878-109">A local store calls **IPSTX::EmulateSpooler** to act as an Outlook Protocol Manager, spooling messages in the outgoing queue to the back-end server (for example, MSN server or AOL server) for processing.</span></span> <span data-ttu-id="04878-110">スプーラーをエミュレートする、同期中に、ストアはし、これら 2 つのメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="04878-110">Emulating a spooler during synchronization, the store then calls these two methods:</span></span> 
  
1. <span data-ttu-id="04878-111">ストア内のメッセージの送信キューを取得するのには**[IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md)** にします。</span><span class="sxs-lookup"><span data-stu-id="04878-111">**[IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md)** to get the outgoing queue of messages in the store.</span></span> <span data-ttu-id="04878-112">このメソッドは、ストアは、Outlook プロトコル マネージャーをエミュレートする場合にのみ成功します。</span><span class="sxs-lookup"><span data-stu-id="04878-112">This method succeeds only if the store is emulating the Outlook Protocol Manager.</span></span> 
    
2. <span data-ttu-id="04878-113">**[IMsgStore::SetLockState](imsgstore-setlockstate.md)** をサーバーに送信する前に、発信キュー内のメッセージにのみアクセスをセキュリティで保護します。</span><span class="sxs-lookup"><span data-stu-id="04878-113">**[IMsgStore::SetLockState](imsgstore-setlockstate.md)** to secure sole access to a message in the outgoing queue just before sending it to the server.</span></span> <span data-ttu-id="04878-114">このメソッドは、ストアは、Outlook プロトコル マネージャーをエミュレートする場合にのみ成功します。</span><span class="sxs-lookup"><span data-stu-id="04878-114">This method succeeds only if the store is emulating the Outlook Protocol Manager.</span></span> <span data-ttu-id="04878-115">メッセージを送信すると、ストアへの唯一のアクセス権を解放するには、再度このメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="04878-115">After sending the message, the store calls this method again to release sole access to it.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="04878-116">Outlook 2002 年以降、Outlook プロトコル マネージャーは MAPI スプーラーを交換してくださいし、バック エンド サーバーに送信メッセージのスプールの担当するようになりました。</span><span class="sxs-lookup"><span data-stu-id="04878-116">Since Outlook 2002, the Outlook Protocol Manager replaced the MAPI spooler and became responsible for spooling outgoing messages to back-end servers.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="04878-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="04878-117">See also</span></span>



[<span data-ttu-id="04878-118">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="04878-118">IPSTX::GetLastError</span></span>](ipstx-getlasterror.md)
  
[<span data-ttu-id="04878-119">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="04878-119">IPSTX::GetSyncObject</span></span>](ipstx-getsyncobject.md)

