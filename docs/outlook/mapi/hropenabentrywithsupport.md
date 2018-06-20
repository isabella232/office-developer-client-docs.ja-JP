---
title: HrOpenABEntryWithSupport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eaa988ea-aee1-4066-8c78-2b6c28def5e0
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 262b1aa2cd4a785b612ac0917b4b24358742ea6f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800329"
---
# <a name="hropenabentrywithsupport"></a><span data-ttu-id="3ffd2-103">HrOpenABEntryWithSupport</span><span class="sxs-lookup"><span data-stu-id="3ffd2-103">HrOpenABEntryWithSupport</span></span>

  
  
<span data-ttu-id="3ffd2-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3ffd2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3ffd2-105">この関数を使用することはしません。</span><span class="sxs-lookup"><span data-stu-id="3ffd2-105">Do not use this function.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3ffd2-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="3ffd2-106">Header file:</span></span>  <br/> |<span data-ttu-id="3ffd2-107">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="3ffd2-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="3ffd2-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="3ffd2-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="3ffd2-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="3ffd2-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="3ffd2-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3ffd2-110">Called by:</span></span>  <br/> |<span data-ttu-id="3ffd2-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="3ffd2-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithSupport(
  LPMAPISUP lpSup,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID  lpInterface,
  ULONG  ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="3ffd2-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="3ffd2-112">Parameters</span></span>

 <span data-ttu-id="3ffd2-113">_lpSup_</span><span class="sxs-lookup"><span data-stu-id="3ffd2-113">_lpSup_</span></span>
  
> 
    
 <span data-ttu-id="3ffd2-114">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="3ffd2-114">_cbEntryID_</span></span>
  
> <span data-ttu-id="3ffd2-115">[in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="3ffd2-115">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="3ffd2-116">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="3ffd2-116">_lpEntryID_</span></span>
  
> <span data-ttu-id="3ffd2-117">[in]開くにはアドレス帳のエントリを表すエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="3ffd2-117">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="3ffd2-118">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="3ffd2-118">_lpInterface_</span></span>
  
>  <span data-ttu-id="3ffd2-119">[in][Open] エントリにアクセスするために使用するインターフェイスのインターフェイス id (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="3ffd2-119">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="3ffd2-120">NULL を渡すことは、標準的なオブジェクトのインターフェイスを返します。</span><span class="sxs-lookup"><span data-stu-id="3ffd2-120">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="3ffd2-121">メッセージング ユーザーは、標準のインタ フェースは[IMailUser: IMAPIProp](imailuserimapiprop.md)。</span><span class="sxs-lookup"><span data-stu-id="3ffd2-121">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="3ffd2-122">配布リスト、 [IDistList: IMAPIContainer](idistlistimapicontainer.md)では、コンテナー、および[これにより: IMAPIContainer](iabcontainerimapicontainer.md)。</span><span class="sxs-lookup"><span data-stu-id="3ffd2-122">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="3ffd2-123">呼び出し元は、適切な標準インターフェイスまたはインターフェイスの継承階層内に_lpInterface_を設定できます。</span><span class="sxs-lookup"><span data-stu-id="3ffd2-123">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="3ffd2-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3ffd2-124">_ulFlags_</span></span>
  
> <span data-ttu-id="3ffd2-125">[in]_LpszButtonText_パラメーターのテキストの種類を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="3ffd2-125">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="3ffd2-126">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="3ffd2-126">The following flags can be set:</span></span> 
    
<span data-ttu-id="3ffd2-127">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="3ffd2-127">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="3ffd2-128">詳細は TRUE を返す場合は、アドレスに変更を加えた実際にことを示します。それ以外の場合、詳細は、FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="3ffd2-128">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="3ffd2-129">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="3ffd2-129">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="3ffd2-130">共通のアドレス] ダイアログ ボックスのモーダル バージョンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3ffd2-130">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="3ffd2-131">このフラグは、DIALOG_SDI と相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="3ffd2-131">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="3ffd2-132">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="3ffd2-132">DIALOG_SDI</span></span>
  
> <span data-ttu-id="3ffd2-133">モードレスのバージョンの共通のアドレス] ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3ffd2-133">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="3ffd2-134">このフラグは、DIALOG_MODAL と相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="3ffd2-134">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="3ffd2-135">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3ffd2-135">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="3ffd2-136">渡された文字列は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="3ffd2-136">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="3ffd2-137">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="3ffd2-137">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="3ffd2-138">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="3ffd2-138">_lpulObjType_</span></span>
  
> <span data-ttu-id="3ffd2-139">[out]開かれているエントリの種類へのポインター。</span><span class="sxs-lookup"><span data-stu-id="3ffd2-139">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="3ffd2-140">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="3ffd2-140">_lppUnk_</span></span>
  
> <span data-ttu-id="3ffd2-141">[out]開かれているエントリのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="3ffd2-141">[out] A pointer to a pointer of the opened entry.</span></span>
    

