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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 024583926b5d0be638b33b1b60c5d4c5dc74d05b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438954"
---
# <a name="ipstxemulatespooler"></a><span data-ttu-id="2266a-103">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="2266a-103">IPSTX::EmulateSpooler</span></span>

  
  
<span data-ttu-id="2266a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2266a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2266a-105">Outlook プロトコルマネージャーをエミュレートして、送信メッセージをサーバーにスプールするように、ローカルストアを設定します。</span><span class="sxs-lookup"><span data-stu-id="2266a-105">Sets a local store to emulate the Outlook Protocol Manager to spool outgoing messages to a server.</span></span>
  
```cpp
HRESULT EmulateSpooler( 
    BOOL fEmulate 
);
```

 <span data-ttu-id="2266a-106">_femulate_</span><span class="sxs-lookup"><span data-stu-id="2266a-106">_fEmulate_</span></span>
  
>  <span data-ttu-id="2266a-107">順番ローカルストアがスプーラーをエミュレートする必要がある場合は、このパラメーターを True に設定します。そうでない場合は False に設定します。</span><span class="sxs-lookup"><span data-stu-id="2266a-107">[in] Set this parameter to True if the local store should emulate the spooler; set it to False if not.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2266a-108">注釈</span><span class="sxs-lookup"><span data-stu-id="2266a-108">Remarks</span></span>

<span data-ttu-id="2266a-109">ローカルストアは**ipstx:: EmulateSpooler**を呼び出して、Outlook プロトコルマネージャーとして機能し、送信キュー内のメッセージをバックエンドサーバー (たとえば、MSN server または AOL サーバー) にスプールして処理します。</span><span class="sxs-lookup"><span data-stu-id="2266a-109">A local store calls **IPSTX::EmulateSpooler** to act as an Outlook Protocol Manager, spooling messages in the outgoing queue to the back-end server (for example, MSN server or AOL server) for processing.</span></span> <span data-ttu-id="2266a-110">同期時にスプーラーをエミュレートすると、ストアは次の2つのメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2266a-110">Emulating a spooler during synchronization, the store then calls these two methods:</span></span> 
  
1. <span data-ttu-id="2266a-111">**[IMsgStore:: getoutgoingqueue](imsgstore-getoutgoingqueue.md)** ストア内のメッセージの送信キューを取得します。</span><span class="sxs-lookup"><span data-stu-id="2266a-111">**[IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md)** to get the outgoing queue of messages in the store.</span></span> <span data-ttu-id="2266a-112">このメソッドは、ストアが Outlook プロトコルマネージャーをエミュレートしている場合にのみ成功します。</span><span class="sxs-lookup"><span data-stu-id="2266a-112">This method succeeds only if the store is emulating the Outlook Protocol Manager.</span></span> 
    
2. <span data-ttu-id="2266a-113">**[IMsgStore:: SetLockState](imsgstore-setlockstate.md)** は、メッセージをサーバーに送信する直前に、送信キュー内のメッセージへのアクセスを保護します。</span><span class="sxs-lookup"><span data-stu-id="2266a-113">**[IMsgStore::SetLockState](imsgstore-setlockstate.md)** to secure sole access to a message in the outgoing queue just before sending it to the server.</span></span> <span data-ttu-id="2266a-114">このメソッドは、ストアが Outlook プロトコルマネージャーをエミュレートしている場合にのみ成功します。</span><span class="sxs-lookup"><span data-stu-id="2266a-114">This method succeeds only if the store is emulating the Outlook Protocol Manager.</span></span> <span data-ttu-id="2266a-115">メッセージを送信した後、ストアはこのメソッドをもう一度呼び出して、単独でアクセス権を解放します。</span><span class="sxs-lookup"><span data-stu-id="2266a-115">After sending the message, the store calls this method again to release sole access to it.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="2266a-116">outlook 2002 以降、outlook プロトコルマネージャーは MAPI スプーラーを置き換え、送信メッセージをバックエンドサーバーにスプールする責任がありました。</span><span class="sxs-lookup"><span data-stu-id="2266a-116">Since Outlook 2002, the Outlook Protocol Manager replaced the MAPI spooler and became responsible for spooling outgoing messages to back-end servers.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2266a-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="2266a-117">See also</span></span>



[<span data-ttu-id="2266a-118">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="2266a-118">IPSTX::GetLastError</span></span>](ipstx-getlasterror.md)
  
[<span data-ttu-id="2266a-119">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="2266a-119">IPSTX::GetSyncObject</span></span>](ipstx-getsyncobject.md)

