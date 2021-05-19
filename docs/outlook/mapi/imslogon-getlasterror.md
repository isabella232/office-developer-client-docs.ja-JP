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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425877"
---
# <a name="imslogongetlasterror"></a><span data-ttu-id="9be76-103">IMSLogon::GetLastError</span><span class="sxs-lookup"><span data-stu-id="9be76-103">IMSLogon::GetLastError</span></span>

  
  
<span data-ttu-id="9be76-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9be76-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9be76-105">メッセージ ストア オブジェクト [に対して](mapierror.md) 発生した最後のエラーに関する情報を含む MAPIERROR 構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="9be76-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for the message store object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="9be76-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9be76-106">Parameters</span></span>

 <span data-ttu-id="9be76-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="9be76-107">_hResult_</span></span>
  
> <span data-ttu-id="9be76-108">[in]メッセージ ストア オブジェクトの前のメソッド呼び出しで生成されたエラー値を含む HRESULT データ型。</span><span class="sxs-lookup"><span data-stu-id="9be76-108">[in] An HRESULT data type that contains the error value generated in the previous method call for the message store object.</span></span>
    
 <span data-ttu-id="9be76-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9be76-109">_ulFlags_</span></span>
  
> <span data-ttu-id="9be76-110">[in]返される文字列の種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="9be76-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="9be76-111">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="9be76-111">The following flag can be set:</span></span>
    
<span data-ttu-id="9be76-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9be76-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="9be76-113">_lppMAPIError_ パラメーターで返される **MAPIERROR** 構造体の文字列は、Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="9be76-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="9be76-114">このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="9be76-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="9be76-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="9be76-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="9be76-116">[out]エラーのバージョン、コンポーネント、コンテキスト情報を含む、返される **MAPIERROR** 構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="9be76-116">[out] A pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="9be76-117">_戻す MAPIERROR がない場合は、lppMAPIError_ パラメーター **を NULL に** 設定できます。</span><span class="sxs-lookup"><span data-stu-id="9be76-117">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9be76-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="9be76-118">Return value</span></span>

<span data-ttu-id="9be76-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="9be76-119">S_OK</span></span> 
  
> <span data-ttu-id="9be76-120">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="9be76-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="9be76-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="9be76-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="9be76-122">このフラグMAPI_UNICODE設定され、実装が Unicode をサポートしていないか、または設定されていないMAPI_UNICODE実装が Unicode のみをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="9be76-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9be76-123">注釈</span><span class="sxs-lookup"><span data-stu-id="9be76-123">Remarks</span></span>

<span data-ttu-id="9be76-124">**IMSLogon::GetLastError** メソッドを使用して、メッセージ ストア オブジェクトのメソッド呼び出しから返された最後のエラーに関する情報をユーザーにメッセージで表示します。</span><span class="sxs-lookup"><span data-stu-id="9be76-124">Use the **IMSLogon::GetLastError** method to retrieve information to display in a message to the user regarding the last error returned from a method call for the message store object.</span></span> 
  
<span data-ttu-id="9be76-125">返される **MAPIERROR** 構造に対して MAPI によって割り当てられたすべてのメモリを解放するには、クライアント アプリケーションが [MAPIFreeBuffer](mapifreebuffer.md) 関数のみを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="9be76-125">To release all the memory allocated by MAPI for the returned **MAPIERROR** structure, client applications need to call only the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="9be76-126">アプリケーションが MAPIERROR を使用するには **、GetLastError** S_OK戻り値を使用する **必要があります**。</span><span class="sxs-lookup"><span data-stu-id="9be76-126">The return value from **GetLastError** must be S_OK for an application to use the **MAPIERROR**.</span></span> <span data-ttu-id="9be76-127">戻り値が指定S_OK **MAPIERROR** が返されない場合があります。</span><span class="sxs-lookup"><span data-stu-id="9be76-127">Even if the return value is S_OK, a **MAPIERROR** might not be returned.</span></span> <span data-ttu-id="9be76-128">実装で最後のエラーが何だったのか判断できない場合、または **MAPIERROR** がエラーに対して使用できない場合 **、GetLastError** は  _代わりに lppMAPIError_ で NULL へのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="9be76-128">If the implementation cannot determine what the last error was, or if a **MAPIERROR** is not available for that error, **GetLastError** returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9be76-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="9be76-129">See also</span></span>



[<span data-ttu-id="9be76-130">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="9be76-130">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="9be76-131">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="9be76-131">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="9be76-132">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9be76-132">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

