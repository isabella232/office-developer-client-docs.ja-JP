---
title: HRESULT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HRESULT
api_type:
- COM
ms.assetid: b248ed11-3d8a-4d4c-9b84-fa5bee7979c7
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 64fcbebbd71bc3f478f36c711e49db9a3518ef9a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435020"
---
# <a name="hresult"></a><span data-ttu-id="a6dd3-103">HRESULT</span><span class="sxs-lookup"><span data-stu-id="a6dd3-103">HRESULT</span></span>

  
  
<span data-ttu-id="a6dd3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6dd3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a6dd3-105">エラーまたは警告を記述するために使用される32ビット値。</span><span class="sxs-lookup"><span data-stu-id="a6dd3-105">A 32-bit value that is used to describe an error or warning.</span></span>
  
```cpp
typedef LONG HRESULT;
```

## <a name="remarks"></a><span data-ttu-id="a6dd3-106">注釈</span><span class="sxs-lookup"><span data-stu-id="a6dd3-106">Remarks</span></span>

<span data-ttu-id="a6dd3-107">**HRESULT**データ型は、 [SCODE](scode.md)データ型と同じです。</span><span class="sxs-lookup"><span data-stu-id="a6dd3-107">The **HRESULT** data type is the same as the [SCODE](scode.md) data type.</span></span> 
  
<span data-ttu-id="a6dd3-108">**HRESULT**値は、次のフィールドで構成されます。</span><span class="sxs-lookup"><span data-stu-id="a6dd3-108">An **HRESULT** value consists of the following fields:</span></span> 
  
- <span data-ttu-id="a6dd3-109">重要度を示す1ビットのコード。0は成功を、1はエラーを表します。</span><span class="sxs-lookup"><span data-stu-id="a6dd3-109">A 1-bit code indicating severity, where zero represents success and 1 represents failure.</span></span>
    
- <span data-ttu-id="a6dd3-110">4ビット予約値。</span><span class="sxs-lookup"><span data-stu-id="a6dd3-110">A 4-bit reserved value.</span></span>
    
- <span data-ttu-id="a6dd3-111">エラーまたは警告 (ファシリティコードとも呼ばれる) の責任を示す11ビットのコード。</span><span class="sxs-lookup"><span data-stu-id="a6dd3-111">An 11-bit code indicating responsibility for the error or warning, also known as a facility code.</span></span>
    
- <span data-ttu-id="a6dd3-112">エラーまたは警告を説明する16ビットコード。</span><span class="sxs-lookup"><span data-stu-id="a6dd3-112">A 16-bit code describing the error or warning.</span></span>
    
<span data-ttu-id="a6dd3-113">ほとんどの MAPI インターフェイスのメソッドと関数は、 **HRESULT**値を返して詳細な原因のフォーメーションを提供します。</span><span class="sxs-lookup"><span data-stu-id="a6dd3-113">Most MAPI interface methods and functions return **HRESULT** values to provide detailed cause formation.</span></span> <span data-ttu-id="a6dd3-114">**HRESULT**値は、OLE インターフェイスメソッドでも広く使用されています。</span><span class="sxs-lookup"><span data-stu-id="a6dd3-114">**HRESULT** values are also used widely in OLE interface methods.</span></span> <span data-ttu-id="a6dd3-115">OLE には、 **HRESULT**値と**SCODE**値の間で変換するためのマクロがいくつか用意されています。エラー処理には別の一般的なデータ型があります。</span><span class="sxs-lookup"><span data-stu-id="a6dd3-115">OLE provides several macros for converting between **HRESULT** values and **SCODE** values, another common data type for error handling.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a6dd3-116">64ビット MAPI では、 **HRESULT**は32ビット値のままです。</span><span class="sxs-lookup"><span data-stu-id="a6dd3-116">In 64-bit MAPI, **HRESULT** is still a 32-bit value.</span></span> 
  
<span data-ttu-id="a6dd3-117">**HRESULT**値の ole 使用法については、「 *ole プログラマーズリファレンス*」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a6dd3-117">For information about the OLE use of **HRESULT** values, see the  *OLE Programmer's Reference*  .</span></span> <span data-ttu-id="a6dd3-118">これらの値の MAPI での使用の詳細については、「[エラー処理](error-handling-in-mapi.md)」および次のいずれかのインターフェイスメソッドを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a6dd3-118">For more information about the use of these values in MAPI, see [Error Handling](error-handling-in-mapi.md) and any of the following interface methods:</span></span> 
  
[<span data-ttu-id="a6dd3-119">IABLogon::GetLastError</span><span class="sxs-lookup"><span data-stu-id="a6dd3-119">IABLogon::GetLastError</span></span>](iablogon-getlasterror.md)
  
[<span data-ttu-id="a6dd3-120">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="a6dd3-120">IMAPISupport::GetLastError</span></span>](imapisupport-getlasterror.md)
  
[<span data-ttu-id="a6dd3-121">IMAPIControl::GetLastError</span><span class="sxs-lookup"><span data-stu-id="a6dd3-121">IMAPIControl::GetLastError</span></span>](imapicontrol-getlasterror.md)
  
[<span data-ttu-id="a6dd3-122">IMAPITable::GetLastError</span><span class="sxs-lookup"><span data-stu-id="a6dd3-122">IMAPITable::GetLastError</span></span>](imapitable-getlasterror.md)
  
[<span data-ttu-id="a6dd3-123">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="a6dd3-123">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="a6dd3-124">IMAPIViewAdviseSink::OnPrint</span><span class="sxs-lookup"><span data-stu-id="a6dd3-124">IMAPIViewAdviseSink::OnPrint</span></span>](imapiviewadvisesink-onprint.md)
  
## <a name="see-also"></a><span data-ttu-id="a6dd3-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="a6dd3-125">See also</span></span>



[<span data-ttu-id="a6dd3-126">SCODE</span><span class="sxs-lookup"><span data-stu-id="a6dd3-126">SCODE</span></span>](scode.md)


[<span data-ttu-id="a6dd3-127">MAPI のデータ型</span><span class="sxs-lookup"><span data-stu-id="a6dd3-127">MAPI Data Types</span></span>](mapi-data-types.md)

