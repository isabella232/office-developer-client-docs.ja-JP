---
title: IMAPISessionGetLastError
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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 59b534a076aee6498be9146eabb69c62fca313ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800681"
---
# <a name="imapisessiongetlasterror"></a><span data-ttu-id="0c940-103">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="0c940-103">IMAPISession::GetLastError</span></span>

  
  
<span data-ttu-id="0c940-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0c940-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0c940-105">前のセッションのエラーに関する情報を含む[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="0c940-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous session error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="0c940-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0c940-106">Parameters</span></span>

 <span data-ttu-id="0c940-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="0c940-107">_hResult_</span></span>
  
> <span data-ttu-id="0c940-108">[in]以前のメソッドの呼び出しで生成されたエラーの値へのハンドル。</span><span class="sxs-lookup"><span data-stu-id="0c940-108">[in] A handle to the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="0c940-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0c940-109">_ulFlags_</span></span>
  
> <span data-ttu-id="0c940-110">[in]返される文字列の種類を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="0c940-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="0c940-111">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="0c940-111">The following flag can be set:</span></span>
    
<span data-ttu-id="0c940-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0c940-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="0c940-113">_LppMAPIError_パラメーターに返された**MAPIERROR**構造体の文字列は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="0c940-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="0c940-114">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="0c940-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="0c940-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="0c940-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="0c940-116">[out]エラーのバージョン、コンポーネント、およびコンテキストの情報を格納する**MAPIERROR**構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="0c940-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="0c940-117">MAPI は、 **MAPIERROR**構造体の適切な情報を提供できない場合、 _lppMAPIError_パラメーターを NULL に設定できます。</span><span class="sxs-lookup"><span data-stu-id="0c940-117">The  _lppMAPIError_ parameter can be set to NULL if MAPI cannot supply appropriate information for a **MAPIERROR** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0c940-118">�߂�l</span><span class="sxs-lookup"><span data-stu-id="0c940-118">Return value</span></span>

<span data-ttu-id="0c940-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="0c940-119">S_OK</span></span> 
  
> <span data-ttu-id="0c940-120">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="0c940-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="0c940-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="0c940-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="0c940-122">MAPI_UNICODE フラグが設定され、セッションが Unicode をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="0c940-122">The MAPI_UNICODE flag was set and the session does not support Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0c940-123">注釈</span><span class="sxs-lookup"><span data-stu-id="0c940-123">Remarks</span></span>

<span data-ttu-id="0c940-124">**IMAPISession::GetLastError**メソッドは、 **IMAPISession**メソッドの呼び出しによって返された最後のエラーに関する情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="0c940-124">The **IMAPISession::GetLastError** method retrieves information about the last error that was returned by an **IMAPISession** method call.</span></span> <span data-ttu-id="0c940-125">クライアントは、ダイアログ ボックスでこの情報を含めることによって、エラーの詳細情報をユーザーを提供できます。</span><span class="sxs-lookup"><span data-stu-id="0c940-125">Clients can provide their users with detailed information about the error by including this information in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0c940-126">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="0c940-126">Notes to callers</span></span>

<span data-ttu-id="0c940-127">MAPI が提供を 1 つ**返します**は S_OK を返し、 _lppMAPIError_パラメーター場合にのみが指す場合は、 **MAPIERROR**構造体を使用できます。</span><span class="sxs-lookup"><span data-stu-id="0c940-127">You can use the **MAPIERROR** structure, if MAPI supplies one, pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="0c940-128">場合があります、MAPI ではその最後のエラーを判断できないか、エラーの報告には関係ありません。</span><span class="sxs-lookup"><span data-stu-id="0c940-128">Sometimes MAPI cannot determine what the last error was, or it has nothing more to report about the error.</span></span> <span data-ttu-id="0c940-129">このような場合は、 **GetLastError**のポインターを返します NULL に_lppMAPIError_の代わりにします。</span><span class="sxs-lookup"><span data-stu-id="0c940-129">In this situation, **GetLastError** returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="0c940-130">**GetLastError**メソッドの詳細については、 [MAPI の拡張エラー](mapi-extended-errors.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0c940-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0c940-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="0c940-131">See also</span></span>



[<span data-ttu-id="0c940-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="0c940-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="0c940-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="0c940-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="0c940-134">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="0c940-134">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


<span data-ttu-id="0c940-135">[MAPI �g���G���[](mapi-extended-errors.md)</span><span class="sxs-lookup"><span data-stu-id="0c940-135">[MAPI Extended Errors](mapi-extended-errors.md)</span></span>

