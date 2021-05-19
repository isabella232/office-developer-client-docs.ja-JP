---
title: HrOpenABEntryWithSupport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eaa988ea-aee1-4066-8c78-2b6c28def5e0
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b8574264bdb470906cc097cec56b39a943937d11
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417645"
---
# <a name="hropenabentrywithsupport"></a><span data-ttu-id="0400f-103">HrOpenABEntryWithSupport</span><span class="sxs-lookup"><span data-stu-id="0400f-103">HrOpenABEntryWithSupport</span></span>

  
  
<span data-ttu-id="0400f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0400f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0400f-105">この関数は使用しません。</span><span class="sxs-lookup"><span data-stu-id="0400f-105">Do not use this function.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0400f-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="0400f-106">Header file:</span></span>  <br/> |<span data-ttu-id="0400f-107">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="0400f-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="0400f-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="0400f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0400f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0400f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0400f-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="0400f-110">Called by:</span></span>  <br/> |<span data-ttu-id="0400f-111">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="0400f-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="0400f-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0400f-112">Parameters</span></span>

 <span data-ttu-id="0400f-113">_lpSup_</span><span class="sxs-lookup"><span data-stu-id="0400f-113">_lpSup_</span></span>
  
> 
    
 <span data-ttu-id="0400f-114">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="0400f-114">_cbEntryID_</span></span>
  
> <span data-ttu-id="0400f-115">[in]  _lpEntryID_ パラメーターで指定されたエントリ識別子のバイト 数。</span><span class="sxs-lookup"><span data-stu-id="0400f-115">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="0400f-116">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="0400f-116">_lpEntryID_</span></span>
  
> <span data-ttu-id="0400f-117">[in]開くアドレス帳エントリを表すエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="0400f-117">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="0400f-118">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="0400f-118">_lpInterface_</span></span>
  
>  <span data-ttu-id="0400f-119">[in]開いているエントリへのアクセスに使用するインターフェイスのインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="0400f-119">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="0400f-120">NULL を渡す場合は、オブジェクトの標準インターフェイスを返します。</span><span class="sxs-lookup"><span data-stu-id="0400f-120">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="0400f-121">メッセージング ユーザーの場合、標準インターフェイスは [IMailUser : IMAPIProp です](imailuserimapiprop.md)。</span><span class="sxs-lookup"><span data-stu-id="0400f-121">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="0400f-122">配布リストの場合 [、IDistList : IMAPIContainer](idistlistimapicontainer.md)であり、コンテナーの場合は [IABContainer : IMAPIContainer です](iabcontainerimapicontainer.md)。</span><span class="sxs-lookup"><span data-stu-id="0400f-122">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="0400f-123">呼び出し元は  _、lpInterface を_ 適切な標準インターフェイスまたは継承階層内のインターフェイスに設定できます。</span><span class="sxs-lookup"><span data-stu-id="0400f-123">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="0400f-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0400f-124">_ulFlags_</span></span>
  
> <span data-ttu-id="0400f-125">[in]  _lpszButtonText_ パラメーターのテキストの種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="0400f-125">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="0400f-126">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="0400f-126">The following flags can be set:</span></span> 
    
<span data-ttu-id="0400f-127">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="0400f-127">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="0400f-128">アドレスに実際に変更が加えた場合、Details は TRUE を返します。それ以外の場合、Details は FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="0400f-128">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="0400f-129">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="0400f-129">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="0400f-130">[共通アドレス] ダイアログ ボックスのモーダル バージョンを表示します。</span><span class="sxs-lookup"><span data-stu-id="0400f-130">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="0400f-131">このフラグは、このフラグと相互にDIALOG_SDI。</span><span class="sxs-lookup"><span data-stu-id="0400f-131">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="0400f-132">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="0400f-132">DIALOG_SDI</span></span>
  
> <span data-ttu-id="0400f-133">[共通アドレス] ダイアログ ボックスのモードレス バージョンを表示します。</span><span class="sxs-lookup"><span data-stu-id="0400f-133">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="0400f-134">このフラグは、他のフラグと相互DIALOG_MODAL。</span><span class="sxs-lookup"><span data-stu-id="0400f-134">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="0400f-135">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0400f-135">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="0400f-136">渡された文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="0400f-136">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="0400f-137">このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="0400f-137">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="0400f-138">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="0400f-138">_lpulObjType_</span></span>
  
> <span data-ttu-id="0400f-139">[out]開いたエントリの種類へのポインター。</span><span class="sxs-lookup"><span data-stu-id="0400f-139">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="0400f-140">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="0400f-140">_lppUnk_</span></span>
  
> <span data-ttu-id="0400f-141">[out]開いたエントリのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="0400f-141">[out] A pointer to a pointer of the opened entry.</span></span>
    

