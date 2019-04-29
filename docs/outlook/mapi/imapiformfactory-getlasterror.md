---
title: IMAPIFormFactoryGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory.GetLastError
api_type:
- COM
ms.assetid: 4b1d85f6-7996-4839-b985-abf83e305651
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2c83f7788d9c01ab02f1a2bc39a35abe2c5a21c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417009"
---
# <a name="imapiformfactorygetlasterror"></a><span data-ttu-id="b2727-103">IMAPIFormFactory::GetLastError</span><span class="sxs-lookup"><span data-stu-id="b2727-103">IMAPIFormFactory::GetLastError</span></span>

  
  
<span data-ttu-id="b2727-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b2727-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b2727-105">form factory オブジェクトに発生する前のエラーについての情報を含む[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="b2727-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form factory object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="b2727-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b2727-106">Parameters</span></span>

 <span data-ttu-id="b2727-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="b2727-107">_hResult_</span></span>
  
> <span data-ttu-id="b2727-108">順番前のメソッド呼び出しで生成されたエラー値を含む HRESULT データ型。</span><span class="sxs-lookup"><span data-stu-id="b2727-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="b2727-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b2727-109">_ulFlags_</span></span>
  
> <span data-ttu-id="b2727-110">順番返される文字列の種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="b2727-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="b2727-111">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="b2727-111">The following flag can be set:</span></span> 
    
<span data-ttu-id="b2727-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b2727-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="b2727-113">_lppMAPIError_パラメーターで返される**MAPIERROR**構造体の文字列は、Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="b2727-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="b2727-114">MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="b2727-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="b2727-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="b2727-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="b2727-116">読み上げエラーのバージョン、コンポーネント、およびコンテキスト情報を含む、返された**MAPIERROR**構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="b2727-116">[out] A pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="b2727-117">**MAPIERROR**構造体を返さない場合は、このパラメーターを NULL に設定できます。</span><span class="sxs-lookup"><span data-stu-id="b2727-117">This parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b2727-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="b2727-118">Return value</span></span>

<span data-ttu-id="b2727-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="b2727-119">S_OK</span></span> 
  
> <span data-ttu-id="b2727-120">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="b2727-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="b2727-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="b2727-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="b2727-122">MAPI_UNICODE フラグが設定されていて、 **getlasterror**が unicode をサポートしていないか、または MAPI_UNICODE が設定されておらず、 **getlasterror**が unicode のみをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="b2727-122">Either the MAPI_UNICODE flag was set and **GetLastError** does not support Unicode, or MAPI_UNICODE was not set and **GetLastError** supports only Unicode.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b2727-123">注釈</span><span class="sxs-lookup"><span data-stu-id="b2727-123">Remarks</span></span>

<span data-ttu-id="b2727-124">**imapiformfactory:: GetLastError**メソッドは、失敗した前のメソッド呼び出しに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="b2727-124">The **IMAPIFormFactory::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="b2727-125">呼び出し元は、 **MAPIERROR**構造のデータをダイアログボックスに含めることによって、エラーに関する詳細情報をユーザーに提供できます。</span><span class="sxs-lookup"><span data-stu-id="b2727-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b2727-126">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="b2727-126">Notes to callers</span></span>

<span data-ttu-id="b2727-127">_lppMAPIError_パラメーターでポイントされている**MAPIERROR**構造体は、 **GetLastError**が S_OK を返す場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="b2727-127">You can make use of the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter if MAPI supplies one only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="b2727-128">MAPI では、エラーについてのレポートを作成するために最後のエラーが発生したかどうかを判断できない場合があります。</span><span class="sxs-lookup"><span data-stu-id="b2727-128">Sometimes MAPI cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="b2727-129">このような場合、代わりに_lppMAPIError_で NULL へのポインターが返されます。</span><span class="sxs-lookup"><span data-stu-id="b2727-129">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="b2727-130">**GetLastError**メソッドの詳細については、「[拡張エラーの使用](mapi-extended-errors.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2727-130">For more information about the **GetLastError** method, see [Using Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b2727-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="b2727-131">See also</span></span>



[<span data-ttu-id="b2727-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="b2727-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="b2727-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="b2727-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="b2727-134">IMAPIFormFactory : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b2727-134">IMAPIFormFactory : IUnknown</span></span>](imapiformfactoryiunknown.md)

