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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 22f17df9347b4744dfe6598e7007469ffb9e5251
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801520"
---
# <a name="mapicrashrecovery"></a><span data-ttu-id="c3d44-103">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="c3d44-103">MAPICrashRecovery</span></span>

<span data-ttu-id="c3d44-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c3d44-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c3d44-105">**MAPICrashRecovery**関数は、共有メモリを個人用フォルダー ファイル (PST) またはオフライン フォルダー ファイル (OST) の状態をチェックします。</span><span class="sxs-lookup"><span data-stu-id="c3d44-105">The **MAPICrashRecovery** function checks the state of the Personal Folders file (PST) or Offline Folders file (OST) shared memory.</span></span> <span data-ttu-id="c3d44-106">メモリは、一貫性のある状態では、 **MAPICrashRecovery**関数はデータをディスクに移動して、プロセスが終了するまでに、さらに読み取りまたは書き込みアクセスを防ぐことが。</span><span class="sxs-lookup"><span data-stu-id="c3d44-106">If the memory is in a consistent state, the **MAPICrashRecovery** function moves the data to disk and prevents further read or write access until the process is terminated.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="c3d44-107">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="c3d44-107">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c3d44-108">によってエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="c3d44-108">Exported by:</span></span>  <br/> |<span data-ttu-id="c3d44-109">olmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="c3d44-109">olmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="c3d44-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="c3d44-110">Called by:</span></span>  <br/> |<span data-ttu-id="c3d44-111">クライアント</span><span class="sxs-lookup"><span data-stu-id="c3d44-111">Client</span></span>  <br/> |
|<span data-ttu-id="c3d44-112">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="c3d44-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="c3d44-113">Outlook</span><span class="sxs-lookup"><span data-stu-id="c3d44-113">Outlook</span></span>  <br/> |
   
```cpp
void MAPICrashRecovery(ULONG ulFlags);
```

## <a name="parameters"></a><span data-ttu-id="c3d44-114">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="c3d44-114">Parameters</span></span>

<span data-ttu-id="c3d44-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c3d44-115">_ulFlags_</span></span>
  
> <span data-ttu-id="c3d44-116">[in]MAPI クラッシュ ・ リカバリの実行方法を制御するために使用するフラグです。</span><span class="sxs-lookup"><span data-stu-id="c3d44-116">[in] Flags used to control how the MAPI crash recovery is performed.</span></span> <span data-ttu-id="c3d44-117">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="c3d44-117">The following flags can be set:</span></span>
    
   - <span data-ttu-id="c3d44-118">**MAPICRASH\_回復**: pst ファイルまたは Ost が一貫性のある状態にある場合は、ディスクをロックする読み取りまたは書き込みアクセスを防止するには、pst ファイルまたは Ost のデータを移動します。</span><span class="sxs-lookup"><span data-stu-id="c3d44-118">**MAPICRASH\_RECOVER**: If the PSTs or OSTs are in a consistent state, move the data to disk and lock the PSTs or OSTs to prevent read or write access.</span></span>
    
   - <span data-ttu-id="c3d44-119">**MAPICRASH\_続行**: デバッグ用の pst ファイルまたは Ost のロックを解除します。</span><span class="sxs-lookup"><span data-stu-id="c3d44-119">**MAPICRASH\_CONTINUE**: Unlock the PSTs or OSTs for debugging.</span></span> <span data-ttu-id="c3d44-120">**MAPICRASH_RECOVER**フラグを使用して**MAPICrashRecovery**を呼び出して後で**MAPICrashRecovery**を呼び出す、 **MAPICRASH\_続行**フラグを続行するのにはデバッグを可能にします。</span><span class="sxs-lookup"><span data-stu-id="c3d44-120">After a successful call to **MAPICrashRecovery** with the **MAPICRASH_RECOVER** flag, call **MAPICrashRecovery** with the **MAPICRASH\_CONTINUE** flag to allow debugging to continue.</span></span> 
    
   - <span data-ttu-id="c3d44-121">**MAPICRASH\_SYSTEM_SHUTDOWN**: pst ファイルまたは Ost が一貫性のある状態にある場合は、ディスクをロックする読み取りまたは書き込みアクセスを防止するには、pst ファイルまたは Ost のデータを移動します。</span><span class="sxs-lookup"><span data-stu-id="c3d44-121">**MAPICRASH\_SYSTEM_SHUTDOWN**: If the PSTs or OSTs are in a consistent state, move the data to disk and lock the PSTs or OSTs to prevent read or write access.</span></span> <span data-ttu-id="c3d44-122">Pst ファイルまたは Ost を使用してロックを解除することはできません**MAPICRASH\_続行**。</span><span class="sxs-lookup"><span data-stu-id="c3d44-122">The PSTs or OSTs cannot be unlocked using **MAPICRASH\_CONTINUE**.</span></span> <span data-ttu-id="c3d44-123">組み合わせて使用する必要があります**MAPICRASH\_回復**。</span><span class="sxs-lookup"><span data-stu-id="c3d44-123">Must be used in combination with **MAPICRASH\_RECOVER**.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c3d44-124">備考</span><span class="sxs-lookup"><span data-stu-id="c3d44-124">Remarks</span></span>

<span data-ttu-id="c3d44-125">上位バイト (0xFF000000) は、プロバイダーの特定のクラッシュ復旧のフラグは予約されています。</span><span class="sxs-lookup"><span data-stu-id="c3d44-125">The upper byte (0xFF000000) is reserved for provider specific crash recovery flags.</span></span>
  
<span data-ttu-id="c3d44-126">**MAPICrashRecovery**を呼び出して、 **MAPICRASH\_回復**と**WM_ENDSESSION**メッセージへの応答にフラグを**MAPICRASH_SYSTEM_SHUTDOWN** 。</span><span class="sxs-lookup"><span data-stu-id="c3d44-126">Call **MAPICrashRecovery** with the **MAPICRASH\_RECOVER** and **MAPICRASH_SYSTEM_SHUTDOWN** flags in response to the **WM_ENDSESSION** message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c3d44-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="c3d44-127">See also</span></span>

- [<span data-ttu-id="c3d44-128">MAPI クラッシュ回復 API について</span><span class="sxs-lookup"><span data-stu-id="c3d44-128">About the MAPI Crash Recovery API</span></span>](about-the-mapi-crash-recovery-api.md)
- [<span data-ttu-id="c3d44-129">MAPI クラッシュ回復 API を使用します。</span><span class="sxs-lookup"><span data-stu-id="c3d44-129">Use the MAPI Crash Recovery API</span></span>](how-to-use-the-mapi-crash-recovery-api.md)

