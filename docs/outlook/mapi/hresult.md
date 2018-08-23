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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a3e46732f9b74b9cdf2dc4c961e7b6b66e3d91d4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565229"
---
# <a name="hresult"></a><span data-ttu-id="7df8e-103">HRESULT</span><span class="sxs-lookup"><span data-stu-id="7df8e-103">HRESULT</span></span>

  
  
<span data-ttu-id="7df8e-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7df8e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7df8e-105">エラーまたは警告を記述するために使用される 32 ビット値です。</span><span class="sxs-lookup"><span data-stu-id="7df8e-105">A 32-bit value that is used to describe an error or warning.</span></span>
  
```cpp
typedef LONG HRESULT;
```

## <a name="remarks"></a><span data-ttu-id="7df8e-106">注釈</span><span class="sxs-lookup"><span data-stu-id="7df8e-106">Remarks</span></span>

<span data-ttu-id="7df8e-107">**HRESULT**のデータ型は、 [SCODE](scode.md)のデータ型と同じです。</span><span class="sxs-lookup"><span data-stu-id="7df8e-107">The **HRESULT** data type is the same as the [SCODE](scode.md) data type.</span></span> 
  
<span data-ttu-id="7df8e-108">**HRESULT**値は、次のフィールドで構成されます。</span><span class="sxs-lookup"><span data-stu-id="7df8e-108">An **HRESULT** value consists of the following fields:</span></span> 
  
- <span data-ttu-id="7df8e-109">重大度を示す 1 ビットのコードでは 0 が成功し、1 を表す失敗を表します。</span><span class="sxs-lookup"><span data-stu-id="7df8e-109">A 1-bit code indicating severity, where zero represents success and 1 represents failure.</span></span>
    
- <span data-ttu-id="7df8e-110">4 ビットの予約された値です。</span><span class="sxs-lookup"><span data-stu-id="7df8e-110">A 4-bit reserved value.</span></span>
    
- <span data-ttu-id="7df8e-111">11 ビットは、エラーまたは警告、機能コードとも呼ばれる責任を示すコードです。</span><span class="sxs-lookup"><span data-stu-id="7df8e-111">An 11-bit code indicating responsibility for the error or warning, also known as a facility code.</span></span>
    
- <span data-ttu-id="7df8e-112">エラーを説明するまたは警告の 16 ビット コードです。</span><span class="sxs-lookup"><span data-stu-id="7df8e-112">A 16-bit code describing the error or warning.</span></span>
    
<span data-ttu-id="7df8e-113">ほとんどの MAPI インターフェイスのメソッドおよび関数は、詳細な原因の形成を提供する**HRESULT**値を返します。</span><span class="sxs-lookup"><span data-stu-id="7df8e-113">Most MAPI interface methods and functions return **HRESULT** values to provide detailed cause formation.</span></span> <span data-ttu-id="7df8e-114">**HRESULT**値 OLE インターフェイスのメソッドで広く使用されます。</span><span class="sxs-lookup"><span data-stu-id="7df8e-114">**HRESULT** values are also used widely in OLE interface methods.</span></span> <span data-ttu-id="7df8e-115">OLE は、別の一般的なデータ型のエラー処理の**HRESULT**値と、 **SCODE**値の間を変換するためいくつかのマクロを提供します。</span><span class="sxs-lookup"><span data-stu-id="7df8e-115">OLE provides several macros for converting between **HRESULT** values and **SCODE** values, another common data type for error handling.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7df8e-116">64 ビットの MAPI で**HRESULT**はまだ 32 ビット値です。</span><span class="sxs-lookup"><span data-stu-id="7df8e-116">In 64-bit MAPI, **HRESULT** is still a 32-bit value.</span></span> 
  
<span data-ttu-id="7df8e-117">**HRESULT**値の OLE の使用については、 *OLE プログラマ リファレンス*を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7df8e-117">For information about the OLE use of **HRESULT** values, see the  *OLE Programmer's Reference*  .</span></span> <span data-ttu-id="7df8e-118">MAPI でこれらの値の使用に関する詳細については、[エラーを処理](error-handling-in-mapi.md)し、次のインターフェイスのメソッドのいずれかを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7df8e-118">For more information about the use of these values in MAPI, see [Error Handling](error-handling-in-mapi.md) and any of the following interface methods:</span></span> 
  
[<span data-ttu-id="7df8e-119">IABLogon::GetLastError</span><span class="sxs-lookup"><span data-stu-id="7df8e-119">IABLogon::GetLastError</span></span>](iablogon-getlasterror.md)
  
[<span data-ttu-id="7df8e-120">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="7df8e-120">IMAPISupport::GetLastError</span></span>](imapisupport-getlasterror.md)
  
[<span data-ttu-id="7df8e-121">IMAPIControl::GetLastError</span><span class="sxs-lookup"><span data-stu-id="7df8e-121">IMAPIControl::GetLastError</span></span>](imapicontrol-getlasterror.md)
  
[<span data-ttu-id="7df8e-122">IMAPITable::GetLastError</span><span class="sxs-lookup"><span data-stu-id="7df8e-122">IMAPITable::GetLastError</span></span>](imapitable-getlasterror.md)
  
[<span data-ttu-id="7df8e-123">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="7df8e-123">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="7df8e-124">IMAPIViewAdviseSink::OnPrint</span><span class="sxs-lookup"><span data-stu-id="7df8e-124">IMAPIViewAdviseSink::OnPrint</span></span>](imapiviewadvisesink-onprint.md)
  
## <a name="see-also"></a><span data-ttu-id="7df8e-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="7df8e-125">See also</span></span>



[<span data-ttu-id="7df8e-126">SCODE</span><span class="sxs-lookup"><span data-stu-id="7df8e-126">SCODE</span></span>](scode.md)


[<span data-ttu-id="7df8e-127">MAPI データ型</span><span class="sxs-lookup"><span data-stu-id="7df8e-127">MAPI Data Types</span></span>](mapi-data-types.md)

