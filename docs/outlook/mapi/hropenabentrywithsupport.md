---
title: HrOpenABEntryWithSupport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eaa988ea-aee1-4066-8c78-2b6c28def5e0
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b8574264bdb470906cc097cec56b39a943937d11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347762"
---
# <a name="hropenabentrywithsupport"></a><span data-ttu-id="f459a-103">HrOpenABEntryWithSupport</span><span class="sxs-lookup"><span data-stu-id="f459a-103">HrOpenABEntryWithSupport</span></span>

  
  
<span data-ttu-id="f459a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f459a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f459a-105">この関数は使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="f459a-105">Do not use this function.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f459a-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="f459a-106">Header file:</span></span>  <br/> |<span data-ttu-id="f459a-107">abhelp .h</span><span class="sxs-lookup"><span data-stu-id="f459a-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="f459a-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="f459a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f459a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f459a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f459a-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="f459a-110">Called by:</span></span>  <br/> |<span data-ttu-id="f459a-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="f459a-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="f459a-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f459a-112">Parameters</span></span>

 <span data-ttu-id="f459a-113">_lpsup_</span><span class="sxs-lookup"><span data-stu-id="f459a-113">_lpSup_</span></span>
  
> 
    
 <span data-ttu-id="f459a-114">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="f459a-114">_cbEntryID_</span></span>
  
> <span data-ttu-id="f459a-115">順番_lな tryid_パラメーターで指定されたエントリ id のバイト数。</span><span class="sxs-lookup"><span data-stu-id="f459a-115">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="f459a-116">_lて tryid_</span><span class="sxs-lookup"><span data-stu-id="f459a-116">_lpEntryID_</span></span>
  
> <span data-ttu-id="f459a-117">順番開くアドレス帳のエントリを表すエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f459a-117">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="f459a-118">_lpinterface_</span><span class="sxs-lookup"><span data-stu-id="f459a-118">_lpInterface_</span></span>
  
>  <span data-ttu-id="f459a-119">順番開いているエントリへのアクセスに使用するインターフェイスのインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f459a-119">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="f459a-120">NULL を渡すと、オブジェクトの標準インターフェイスが返されます。</span><span class="sxs-lookup"><span data-stu-id="f459a-120">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="f459a-121">メッセージングユーザーの場合、標準インターフェイスは[imailuser: imapiprop](imailuserimapiprop.md)です。</span><span class="sxs-lookup"><span data-stu-id="f459a-121">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="f459a-122">配布リストの場合、 [idistlist: IMAPIContainer](idistlistimapicontainer.md)、およびコンテナーの場合は、 [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md)になります。</span><span class="sxs-lookup"><span data-stu-id="f459a-122">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="f459a-123">呼び出し元は、 _lpinterface_を適切な標準インターフェイスまたは継承階層内のインターフェイスに設定できます。</span><span class="sxs-lookup"><span data-stu-id="f459a-123">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="f459a-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f459a-124">_ulFlags_</span></span>
  
> <span data-ttu-id="f459a-125">順番_lpszbuttontext_パラメーターのテキストの種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="f459a-125">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="f459a-126">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="f459a-126">The following flags can be set:</span></span> 
    
<span data-ttu-id="f459a-127">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="f459a-127">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="f459a-128">住所に変更が実際に加えられた場合に、詳細が TRUE を返すことを示します。それ以外の場合、詳細は FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="f459a-128">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="f459a-129">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="f459a-129">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="f459a-130">[共通アドレス] ダイアログボックスのモーダルバージョンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f459a-130">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="f459a-131">このフラグは、DIALOG_SDI とは相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="f459a-131">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="f459a-132">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="f459a-132">DIALOG_SDI</span></span>
  
> <span data-ttu-id="f459a-133">[共通アドレス] ダイアログボックスのモードレスバージョンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f459a-133">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="f459a-134">このフラグは、DIALOG_MODAL とは相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="f459a-134">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="f459a-135">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f459a-135">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="f459a-136">渡された文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="f459a-136">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="f459a-137">MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="f459a-137">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="f459a-138">_lpulobjtype_</span><span class="sxs-lookup"><span data-stu-id="f459a-138">_lpulObjType_</span></span>
  
> <span data-ttu-id="f459a-139">読み上げ開かれた項目の種類へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f459a-139">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="f459a-140">_lppunk_</span><span class="sxs-lookup"><span data-stu-id="f459a-140">_lppUnk_</span></span>
  
> <span data-ttu-id="f459a-141">読み上げ開かれたエントリのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="f459a-141">[out] A pointer to a pointer of the opened entry.</span></span>
    

