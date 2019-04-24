---
title: MAPICrashRecovery
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPICrashRecovery
api_type:
- COM
ms.assetid: 4172e2d3-6343-385b-c691-a64c1e198051
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 9efafbac55a2925e04b533e7c08388c026540dff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357303"
---
# <a name="mapicrashrecovery"></a><span data-ttu-id="f6b22-103">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="f6b22-103">MAPICrashRecovery</span></span>

<span data-ttu-id="f6b22-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f6b22-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f6b22-105">**mapicrashrecovery**関数は、個人用フォルダーファイル (PST) またはオフラインフォルダーファイル (OST) の共有メモリの状態をチェックします。</span><span class="sxs-lookup"><span data-stu-id="f6b22-105">The **MAPICrashRecovery** function checks the state of the Personal Folders file (PST) or Offline Folders file (OST) shared memory.</span></span> <span data-ttu-id="f6b22-106">メモリが一貫した状態にある場合、 **mapicrashrecovery**関数はデータをディスクに移動し、プロセスが終了するまで追加の読み取りまたは書き込みアクセスを禁止します。</span><span class="sxs-lookup"><span data-stu-id="f6b22-106">If the memory is in a consistent state, the **MAPICrashRecovery** function moves the data to disk and prevents further read or write access until the process is terminated.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="f6b22-107">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="f6b22-107">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f6b22-108">エクスポート対象:</span><span class="sxs-lookup"><span data-stu-id="f6b22-108">Exported by:</span></span>  <br/> |<span data-ttu-id="f6b22-109">olmapi32</span><span class="sxs-lookup"><span data-stu-id="f6b22-109">olmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="f6b22-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="f6b22-110">Called by:</span></span>  <br/> |<span data-ttu-id="f6b22-111">クライアント</span><span class="sxs-lookup"><span data-stu-id="f6b22-111">Client</span></span>  <br/> |
|<span data-ttu-id="f6b22-112">実装元:</span><span class="sxs-lookup"><span data-stu-id="f6b22-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="f6b22-113">Outlook</span><span class="sxs-lookup"><span data-stu-id="f6b22-113">Outlook</span></span>  <br/> |
   
```cpp
void MAPICrashRecovery(ULONG ulFlags);
```

## <a name="parameters"></a><span data-ttu-id="f6b22-114">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f6b22-114">Parameters</span></span>

<span data-ttu-id="f6b22-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f6b22-115">_ulFlags_</span></span>
  
> <span data-ttu-id="f6b22-116">順番MAPI のクラッシュ回復を実行する方法を制御するために使用されるフラグです。</span><span class="sxs-lookup"><span data-stu-id="f6b22-116">[in] Flags used to control how the MAPI crash recovery is performed.</span></span> <span data-ttu-id="f6b22-117">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="f6b22-117">The following flags can be set:</span></span>
    
   - <span data-ttu-id="f6b22-118">**mapicrash\_の回復**: pst または ost が一貫した状態にある場合は、データをディスクに移動し、pst または ost をロックして読み取りまたは書き込みのアクセスを禁止します。</span><span class="sxs-lookup"><span data-stu-id="f6b22-118">**MAPICRASH\_RECOVER**: If the PSTs or OSTs are in a consistent state, move the data to disk and lock the PSTs or OSTs to prevent read or write access.</span></span>
    
   - <span data-ttu-id="f6b22-119">**mapicrash\_CONTINUE**: デバッグのために pst または ost のロックを解除します。</span><span class="sxs-lookup"><span data-stu-id="f6b22-119">**MAPICRASH\_CONTINUE**: Unlock the PSTs or OSTs for debugging.</span></span> <span data-ttu-id="f6b22-120">**MAPICRASH_RECOVER**フラグを使用して**mapicrashrecovery**を正常に呼び出した後、mapicrash **\_** の**回復**を使用して、デバッグを続行できるようにします。</span><span class="sxs-lookup"><span data-stu-id="f6b22-120">After a successful call to **MAPICrashRecovery** with the **MAPICRASH_RECOVER** flag, call **MAPICrashRecovery** with the **MAPICRASH\_CONTINUE** flag to allow debugging to continue.</span></span> 
    
   - <span data-ttu-id="f6b22-121">**mapicrash\_SYSTEM_SHUTDOWN**: pst または ost が一貫した状態にある場合は、データをディスクに移動し、pst または ost をロックして読み取りまたは書き込みアクセスを禁止します。</span><span class="sxs-lookup"><span data-stu-id="f6b22-121">**MAPICRASH\_SYSTEM_SHUTDOWN**: If the PSTs or OSTs are in a consistent state, move the data to disk and lock the PSTs or OSTs to prevent read or write access.</span></span> <span data-ttu-id="f6b22-122">pst または ost を、 **mapicrash\_の CONTINUE**を使用してロック解除することはできません。</span><span class="sxs-lookup"><span data-stu-id="f6b22-122">The PSTs or OSTs cannot be unlocked using **MAPICRASH\_CONTINUE**.</span></span> <span data-ttu-id="f6b22-123">**mapicrash\_の回復**と組み合わせて使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f6b22-123">Must be used in combination with **MAPICRASH\_RECOVER**.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f6b22-124">解説</span><span class="sxs-lookup"><span data-stu-id="f6b22-124">Remarks</span></span>

<span data-ttu-id="f6b22-125">上位バイト (0xFF000000) は、プロバイダー固有のクラッシュ回復フラグ用に予約されています。</span><span class="sxs-lookup"><span data-stu-id="f6b22-125">The upper byte (0xFF000000) is reserved for provider specific crash recovery flags.</span></span>
  
<span data-ttu-id="f6b22-126">**WM_ENDSESSION**メッセージへの応答として、 **mapicrash\_の RECOVER**および**MAPICRASH_SYSTEM_SHUTDOWN**フラグを使用して、 **mapicrashrecovery**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f6b22-126">Call **MAPICrashRecovery** with the **MAPICRASH\_RECOVER** and **MAPICRASH_SYSTEM_SHUTDOWN** flags in response to the **WM_ENDSESSION** message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f6b22-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="f6b22-127">See also</span></span>

- [<span data-ttu-id="f6b22-128">MAPI クラッシュ回復 API について</span><span class="sxs-lookup"><span data-stu-id="f6b22-128">About the MAPI Crash Recovery API</span></span>](about-the-mapi-crash-recovery-api.md)
- [<span data-ttu-id="f6b22-129">MAPI クラッシュ回復 API を使用する</span><span class="sxs-lookup"><span data-stu-id="f6b22-129">Use the MAPI Crash Recovery API</span></span>](how-to-use-the-mapi-crash-recovery-api.md)

