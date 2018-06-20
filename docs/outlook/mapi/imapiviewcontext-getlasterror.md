---
title: IMAPIViewContextGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetLastError
api_type:
- COM
ms.assetid: 3306e37a-2500-4281-96c3-ca0d5c81909d
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: f7455e9013f3bd9460ae5f4d876c135594840b68
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800870"
---
# <a name="imapiviewcontextgetlasterror"></a><span data-ttu-id="a0e9f-103">IMAPIViewContext::GetLastError</span><span class="sxs-lookup"><span data-stu-id="a0e9f-103">IMAPIViewContext::GetLastError</span></span>

  
  
<span data-ttu-id="a0e9f-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a0e9f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a0e9f-105">ビュー コンテキスト オブジェクトが発生する前のエラーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="a0e9f-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the view context object.</span></span> 
  
```cpp
HRESULT GetLastError(
HRESULT hResult,
ULONG ulFlags,
LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="a0e9f-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="a0e9f-106">Parameters</span></span>

 <span data-ttu-id="a0e9f-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="a0e9f-107">_hResult_</span></span>
  
> <span data-ttu-id="a0e9f-108">[in]以前のメソッドの呼び出しで生成されたエラー値を格納するデータ型を HRESULT です。</span><span class="sxs-lookup"><span data-stu-id="a0e9f-108">[in] HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="a0e9f-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a0e9f-109">_ulFlags_</span></span>
  
> <span data-ttu-id="a0e9f-110">[in]返される文字列の種類を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="a0e9f-110">[in] Bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="a0e9f-111">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="a0e9f-111">The following flag can be set:</span></span>
    
<span data-ttu-id="a0e9f-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a0e9f-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a0e9f-113">_LppMAPIError_パラメーターに返された**MAPIERROR**構造体の文字列は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="a0e9f-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="a0e9f-114">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="a0e9f-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="a0e9f-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="a0e9f-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="a0e9f-116">[out]エラーのバージョン、コンポーネント、およびコンテキストの情報を格納する返された**MAPIERROR**構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a0e9f-116">[out] Pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="a0e9f-117">取得する**MAPIERROR**構造体が存在しない場合、このパラメーターを NULL に設定することができます。</span><span class="sxs-lookup"><span data-stu-id="a0e9f-117">This parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a0e9f-118">�߂�l</span><span class="sxs-lookup"><span data-stu-id="a0e9f-118">Return value</span></span>

<span data-ttu-id="a0e9f-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="a0e9f-119">S_OK</span></span> 
  
> <span data-ttu-id="a0e9f-120">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="a0e9f-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="a0e9f-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="a0e9f-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="a0e9f-122">か、MAPI_UNICODE フラグが設定された**発生しました**が、Unicode をサポートしていませんまたは MAPI_UNICODE が設定されていないと**GetLastError**を Unicode のみサポートしています。</span><span class="sxs-lookup"><span data-stu-id="a0e9f-122">Either the MAPI_UNICODE flag was set and **GetLastError** does not support Unicode, or MAPI_UNICODE was not set and **GetLastError** only supports Unicode.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a0e9f-123">備考</span><span class="sxs-lookup"><span data-stu-id="a0e9f-123">Remarks</span></span>

<span data-ttu-id="a0e9f-124">**IMAPIViewContext::GetLastError**メソッドでは、失敗したメソッド呼び出しに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="a0e9f-124">The **IMAPIViewContext::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="a0e9f-125">呼び出し元は、ダイアログ ボックスに**MAPIERROR**構造体のデータを含めることによって、エラーの詳細情報をユーザーを提供できます。</span><span class="sxs-lookup"><span data-stu-id="a0e9f-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a0e9f-126">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="a0e9f-126">Notes to callers</span></span>

<span data-ttu-id="a0e9f-127">**MAPIERROR**の使用を行うことができます構造が、 _lppMAPIError_パラメーターが指す場合、MAPI では 1 つが提供される**GetLastError**が S_OK を返す場合にのみです。</span><span class="sxs-lookup"><span data-stu-id="a0e9f-127">You can make use of the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter if MAPI supplies one only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="a0e9f-128">どのような最後のエラーまたはエラーを報告するのにはそれ以上には、MAPI は判断できません。</span><span class="sxs-lookup"><span data-stu-id="a0e9f-128">Sometimes MAPI cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="a0e9f-129">このような場合は、NULL へのポインターが返されます_lppMAPIError_の代わりにします。</span><span class="sxs-lookup"><span data-stu-id="a0e9f-129">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="a0e9f-130">**GetLastError**メソッドの詳細については、 [MAPI の拡張エラー](mapi-extended-errors.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0e9f-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a0e9f-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="a0e9f-131">See also</span></span>



[<span data-ttu-id="a0e9f-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="a0e9f-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="a0e9f-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="a0e9f-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="a0e9f-134">IMAPIViewContext: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a0e9f-134">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)

