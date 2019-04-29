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
# <a name="hropenabentrywithsupport"></a><span data-ttu-id="ebadc-103">HrOpenABEntryWithSupport</span><span class="sxs-lookup"><span data-stu-id="ebadc-103">HrOpenABEntryWithSupport</span></span>

  
  
<span data-ttu-id="ebadc-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ebadc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ebadc-105">この関数は使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="ebadc-105">Do not use this function.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ebadc-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="ebadc-106">Header file:</span></span>  <br/> |<span data-ttu-id="ebadc-107">abhelp .h</span><span class="sxs-lookup"><span data-stu-id="ebadc-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="ebadc-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="ebadc-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ebadc-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ebadc-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ebadc-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="ebadc-110">Called by:</span></span>  <br/> |<span data-ttu-id="ebadc-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="ebadc-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="ebadc-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ebadc-112">Parameters</span></span>

 <span data-ttu-id="ebadc-113">_lpsup_</span><span class="sxs-lookup"><span data-stu-id="ebadc-113">_lpSup_</span></span>
  
> 
    
 <span data-ttu-id="ebadc-114">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="ebadc-114">_cbEntryID_</span></span>
  
> <span data-ttu-id="ebadc-115">順番_lな tryid_パラメーターで指定されたエントリ id のバイト数。</span><span class="sxs-lookup"><span data-stu-id="ebadc-115">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="ebadc-116">_lて tryid_</span><span class="sxs-lookup"><span data-stu-id="ebadc-116">_lpEntryID_</span></span>
  
> <span data-ttu-id="ebadc-117">順番開くアドレス帳のエントリを表すエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ebadc-117">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="ebadc-118">_lpinterface_</span><span class="sxs-lookup"><span data-stu-id="ebadc-118">_lpInterface_</span></span>
  
>  <span data-ttu-id="ebadc-119">順番開いているエントリへのアクセスに使用するインターフェイスのインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ebadc-119">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="ebadc-120">NULL を渡すと、オブジェクトの標準インターフェイスが返されます。</span><span class="sxs-lookup"><span data-stu-id="ebadc-120">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="ebadc-121">メッセージングユーザーの場合、標準インターフェイスは[imailuser: imapiprop](imailuserimapiprop.md)です。</span><span class="sxs-lookup"><span data-stu-id="ebadc-121">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="ebadc-122">配布リストの場合、 [idistlist: IMAPIContainer](idistlistimapicontainer.md)、およびコンテナーの場合は、 [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md)になります。</span><span class="sxs-lookup"><span data-stu-id="ebadc-122">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="ebadc-123">呼び出し元は、 _lpinterface_を適切な標準インターフェイスまたは継承階層内のインターフェイスに設定できます。</span><span class="sxs-lookup"><span data-stu-id="ebadc-123">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="ebadc-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ebadc-124">_ulFlags_</span></span>
  
> <span data-ttu-id="ebadc-125">順番_lpszbuttontext_パラメーターのテキストの種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="ebadc-125">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="ebadc-126">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="ebadc-126">The following flags can be set:</span></span> 
    
<span data-ttu-id="ebadc-127">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="ebadc-127">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="ebadc-128">住所に変更が実際に加えられた場合に、詳細が TRUE を返すことを示します。それ以外の場合、詳細は FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="ebadc-128">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="ebadc-129">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="ebadc-129">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="ebadc-130">[共通アドレス] ダイアログボックスのモーダルバージョンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ebadc-130">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="ebadc-131">このフラグは、DIALOG_SDI とは相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="ebadc-131">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="ebadc-132">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="ebadc-132">DIALOG_SDI</span></span>
  
> <span data-ttu-id="ebadc-133">[共通アドレス] ダイアログボックスのモードレスバージョンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ebadc-133">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="ebadc-134">このフラグは、DIALOG_MODAL とは相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="ebadc-134">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="ebadc-135">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ebadc-135">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="ebadc-136">渡された文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="ebadc-136">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="ebadc-137">MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="ebadc-137">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="ebadc-138">_lpulobjtype_</span><span class="sxs-lookup"><span data-stu-id="ebadc-138">_lpulObjType_</span></span>
  
> <span data-ttu-id="ebadc-139">読み上げ開かれた項目の種類へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ebadc-139">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="ebadc-140">_lppunk_</span><span class="sxs-lookup"><span data-stu-id="ebadc-140">_lppUnk_</span></span>
  
> <span data-ttu-id="ebadc-141">読み上げ開かれたエントリのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ebadc-141">[out] A pointer to a pointer of the opened entry.</span></span>
    

