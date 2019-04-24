---
title: IMSLogonGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.GetLastError
api_type:
- COM
ms.assetid: 3e296f6d-4833-4c68-9b84-df0b09878474
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 472502d0f033370b06a69596944350152ab794f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317298"
---
# <a name="imslogongetlasterror"></a><span data-ttu-id="c9173-103">IMSLogon::GetLastError</span><span class="sxs-lookup"><span data-stu-id="c9173-103">IMSLogon::GetLastError</span></span>

  
  
<span data-ttu-id="c9173-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c9173-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c9173-105">メッセージストアオブジェクトに対して発生した最後のエラーについての情報を含む[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="c9173-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for the message store object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="c9173-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c9173-106">Parameters</span></span>

 <span data-ttu-id="c9173-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="c9173-107">_hResult_</span></span>
  
> <span data-ttu-id="c9173-108">順番以前のメソッド呼び出しでメッセージストアオブジェクトに対して生成されたエラー値を含む HRESULT データ型。</span><span class="sxs-lookup"><span data-stu-id="c9173-108">[in] An HRESULT data type that contains the error value generated in the previous method call for the message store object.</span></span>
    
 <span data-ttu-id="c9173-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c9173-109">_ulFlags_</span></span>
  
> <span data-ttu-id="c9173-110">順番返される文字列の種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="c9173-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="c9173-111">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="c9173-111">The following flag can be set:</span></span>
    
<span data-ttu-id="c9173-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c9173-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="c9173-113">_lppMAPIError_パラメーターで返される**MAPIERROR**構造体の文字列は、Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="c9173-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="c9173-114">MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="c9173-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="c9173-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="c9173-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="c9173-116">読み上げエラーのバージョン、コンポーネント、およびコンテキスト情報を含む、返された**MAPIERROR**構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="c9173-116">[out] A pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="c9173-117">返す**MAPIERROR**が存在しない場合は、 _lppMAPIError_パラメーターを NULL に設定できます。</span><span class="sxs-lookup"><span data-stu-id="c9173-117">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c9173-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="c9173-118">Return value</span></span>

<span data-ttu-id="c9173-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="c9173-119">S_OK</span></span> 
  
> <span data-ttu-id="c9173-120">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="c9173-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="c9173-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="c9173-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="c9173-122">MAPI_UNICODE フラグが設定されていて、実装が unicode をサポートしていないか、または MAPI_UNICODE が設定されておらず、実装で unicode のみがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="c9173-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c9173-123">解説</span><span class="sxs-lookup"><span data-stu-id="c9173-123">Remarks</span></span>

<span data-ttu-id="c9173-124">**IMSLogon:: GetLastError**メソッドを使用すると、メッセージにメッセージとして表示される情報を取得するために、メッセージストアオブジェクトに対するメソッド呼び出しから返された最後のエラーに関する情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="c9173-124">Use the **IMSLogon::GetLastError** method to retrieve information to display in a message to the user regarding the last error returned from a method call for the message store object.</span></span> 
  
<span data-ttu-id="c9173-125">返された**MAPIERROR**構造に対して MAPI によって割り当てられたすべてのメモリを解放するには、クライアントアプリケーションは[MAPIFreeBuffer](mapifreebuffer.md)関数のみを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="c9173-125">To release all the memory allocated by MAPI for the returned **MAPIERROR** structure, client applications need to call only the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="c9173-126">アプリケーションが**MAPIERROR**を使用するには、 **GetLastError**の戻り値が S_OK である必要があります。</span><span class="sxs-lookup"><span data-stu-id="c9173-126">The return value from **GetLastError** must be S_OK for an application to use the **MAPIERROR**.</span></span> <span data-ttu-id="c9173-127">戻り値が S_OK の場合でも、 **MAPIERROR**は返されない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c9173-127">Even if the return value is S_OK, a **MAPIERROR** might not be returned.</span></span> <span data-ttu-id="c9173-128">最後のエラーが発生したかどうかを実装が判断できない場合、またはそのエラーに対して**MAPIERROR**が使用できない場合、 **GetLastError**は_lppMAPIError_で NULL へのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="c9173-128">If the implementation cannot determine what the last error was, or if a **MAPIERROR** is not available for that error, **GetLastError** returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c9173-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="c9173-129">See also</span></span>



[<span data-ttu-id="c9173-130">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="c9173-130">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="c9173-131">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="c9173-131">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="c9173-132">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c9173-132">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

