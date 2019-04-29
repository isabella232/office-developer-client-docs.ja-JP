---
title: imapisessiongetlasterror
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.GetLastError
api_type:
- COM
ms.assetid: 38cb3692-a5f8-403a-9615-9bd5868af23c
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7477213ee854be1ae71b47a0c1b339c4c13b6f04
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435580"
---
# <a name="imapisessiongetlasterror"></a><span data-ttu-id="8d125-103">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="8d125-103">IMAPISession::GetLastError</span></span>

  
  
<span data-ttu-id="8d125-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d125-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d125-105">前のセッションエラーに関する情報を含む[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="8d125-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous session error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="8d125-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8d125-106">Parameters</span></span>

 <span data-ttu-id="8d125-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="8d125-107">_hResult_</span></span>
  
> <span data-ttu-id="8d125-108">順番前のメソッド呼び出しで生成されたエラー値へのハンドル。</span><span class="sxs-lookup"><span data-stu-id="8d125-108">[in] A handle to the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="8d125-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8d125-109">_ulFlags_</span></span>
  
> <span data-ttu-id="8d125-110">順番返される文字列の種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="8d125-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="8d125-111">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="8d125-111">The following flag can be set:</span></span>
    
<span data-ttu-id="8d125-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8d125-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="8d125-113">_lppMAPIError_パラメーターで返される**MAPIERROR**構造体の文字列は、Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="8d125-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="8d125-114">MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="8d125-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="8d125-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="8d125-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="8d125-116">読み上げエラーのバージョン、コンポーネント、およびコンテキスト情報を含む**MAPIERROR**構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="8d125-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="8d125-117">MAPI が**MAPIERROR**構造体について適切な情報を提供できない場合は、 _lppMAPIError_パラメーターを NULL に設定できます。</span><span class="sxs-lookup"><span data-stu-id="8d125-117">The  _lppMAPIError_ parameter can be set to NULL if MAPI cannot supply appropriate information for a **MAPIERROR** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8d125-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="8d125-118">Return value</span></span>

<span data-ttu-id="8d125-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="8d125-119">S_OK</span></span> 
  
> <span data-ttu-id="8d125-120">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="8d125-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="8d125-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="8d125-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="8d125-122">MAPI_UNICODE フラグが設定されていて、セッションは UNICODE をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="8d125-122">The MAPI_UNICODE flag was set and the session does not support Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8d125-123">注釈</span><span class="sxs-lookup"><span data-stu-id="8d125-123">Remarks</span></span>

<span data-ttu-id="8d125-124">**imapisession:: GetLastError**メソッドは、 **imapisession**メソッド呼び出しによって返された最後のエラーに関する情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="8d125-124">The **IMAPISession::GetLastError** method retrieves information about the last error that was returned by an **IMAPISession** method call.</span></span> <span data-ttu-id="8d125-125">クライアントは、この情報をダイアログボックスに含めることによって、エラーに関する詳細情報をユーザーに提供できます。</span><span class="sxs-lookup"><span data-stu-id="8d125-125">Clients can provide their users with detailed information about the error by including this information in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8d125-126">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="8d125-126">Notes to callers</span></span>

<span data-ttu-id="8d125-127">**MAPIERROR**構造体は、 _lppMAPIError_パラメーターで指定された MAPI が S_OK を返す場合にのみ\*\*\*\* 使用できます。</span><span class="sxs-lookup"><span data-stu-id="8d125-127">You can use the **MAPIERROR** structure, if MAPI supplies one, pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="8d125-128">MAPI では、最後のエラーが発生したかどうかを判断できない場合や、エラーについてのレポートを持っている場合もあります。</span><span class="sxs-lookup"><span data-stu-id="8d125-128">Sometimes MAPI cannot determine what the last error was, or it has nothing more to report about the error.</span></span> <span data-ttu-id="8d125-129">このような場合、 _lppMAPIError_では、 **GetLastError**は NULL へのポインターを代わりに返します。</span><span class="sxs-lookup"><span data-stu-id="8d125-129">In this situation, **GetLastError** returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="8d125-130">**GetLastError**メソッドの詳細については、「 [MAPI 拡張エラー](mapi-extended-errors.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8d125-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8d125-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="8d125-131">See also</span></span>



[<span data-ttu-id="8d125-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="8d125-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="8d125-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="8d125-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="8d125-134">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="8d125-134">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="8d125-135">MAPI 拡張エラー</span><span class="sxs-lookup"><span data-stu-id="8d125-135">MAPI Extended Errors</span></span>](mapi-extended-errors.md)

