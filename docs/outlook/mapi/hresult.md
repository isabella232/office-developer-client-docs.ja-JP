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
# <a name="hresult"></a><span data-ttu-id="8e5b6-103">HRESULT</span><span class="sxs-lookup"><span data-stu-id="8e5b6-103">HRESULT</span></span>

  
  
<span data-ttu-id="8e5b6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e5b6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e5b6-105">エラーまたは警告の記述に使用される 32 ビットの値。</span><span class="sxs-lookup"><span data-stu-id="8e5b6-105">A 32-bit value that is used to describe an error or warning.</span></span>
  
```cpp
typedef LONG HRESULT;
```

## <a name="remarks"></a><span data-ttu-id="8e5b6-106">注釈</span><span class="sxs-lookup"><span data-stu-id="8e5b6-106">Remarks</span></span>

<span data-ttu-id="8e5b6-107">**HRESULT データ** 型は [SCODE データ型と](scode.md)同じです。</span><span class="sxs-lookup"><span data-stu-id="8e5b6-107">The **HRESULT** data type is the same as the [SCODE](scode.md) data type.</span></span> 
  
<span data-ttu-id="8e5b6-108">**HRESULT 値は**、次のフィールドで構成されます。</span><span class="sxs-lookup"><span data-stu-id="8e5b6-108">An **HRESULT** value consists of the following fields:</span></span> 
  
- <span data-ttu-id="8e5b6-109">重大度を示す 1 ビット コードで、0 は成功を表し、1 は失敗を表します。</span><span class="sxs-lookup"><span data-stu-id="8e5b6-109">A 1-bit code indicating severity, where zero represents success and 1 represents failure.</span></span>
    
- <span data-ttu-id="8e5b6-110">4 ビットの予約値。</span><span class="sxs-lookup"><span data-stu-id="8e5b6-110">A 4-bit reserved value.</span></span>
    
- <span data-ttu-id="8e5b6-111">エラーまたは警告の責任を示す 11 ビット コード (ファシリティ コードとも呼ばれる)。</span><span class="sxs-lookup"><span data-stu-id="8e5b6-111">An 11-bit code indicating responsibility for the error or warning, also known as a facility code.</span></span>
    
- <span data-ttu-id="8e5b6-112">エラーまたは警告を記述する 16 ビット コード。</span><span class="sxs-lookup"><span data-stu-id="8e5b6-112">A 16-bit code describing the error or warning.</span></span>
    
<span data-ttu-id="8e5b6-113">ほとんどの MAPI インターフェイスメソッドと関数は、詳細な原因形成 **を提供するために HRESULT** 値を返します。</span><span class="sxs-lookup"><span data-stu-id="8e5b6-113">Most MAPI interface methods and functions return **HRESULT** values to provide detailed cause formation.</span></span> <span data-ttu-id="8e5b6-114">**HRESULT 値** は、OLE インターフェイス メソッドでも広く使用されています。</span><span class="sxs-lookup"><span data-stu-id="8e5b6-114">**HRESULT** values are also used widely in OLE interface methods.</span></span> <span data-ttu-id="8e5b6-115">OLE には **、HRESULT** 値と **SCODE** 値の間で変換する複数のマクロが含まれています。エラー処理のためのもう 1 つの一般的なデータ型です。</span><span class="sxs-lookup"><span data-stu-id="8e5b6-115">OLE provides several macros for converting between **HRESULT** values and **SCODE** values, another common data type for error handling.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8e5b6-116">64 ビット MAPI では **、HRESULT** は 32 ビット値です。</span><span class="sxs-lookup"><span data-stu-id="8e5b6-116">In 64-bit MAPI, **HRESULT** is still a 32-bit value.</span></span> 
  
<span data-ttu-id="8e5b6-117">**HRESULT** 値の OLE 使用の詳細については *、「OLE プログラマリファレンス」を参照してください*。</span><span class="sxs-lookup"><span data-stu-id="8e5b6-117">For information about the OLE use of **HRESULT** values, see the  *OLE Programmer's Reference*  .</span></span> <span data-ttu-id="8e5b6-118">MAPI でこれらの値を使用する方法の詳細については [、「Error Handling](error-handling-in-mapi.md) and any any the following interface methods」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8e5b6-118">For more information about the use of these values in MAPI, see [Error Handling](error-handling-in-mapi.md) and any of the following interface methods:</span></span> 
  
[<span data-ttu-id="8e5b6-119">IABLogon::GetLastError</span><span class="sxs-lookup"><span data-stu-id="8e5b6-119">IABLogon::GetLastError</span></span>](iablogon-getlasterror.md)
  
[<span data-ttu-id="8e5b6-120">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="8e5b6-120">IMAPISupport::GetLastError</span></span>](imapisupport-getlasterror.md)
  
[<span data-ttu-id="8e5b6-121">IMAPIControl::GetLastError</span><span class="sxs-lookup"><span data-stu-id="8e5b6-121">IMAPIControl::GetLastError</span></span>](imapicontrol-getlasterror.md)
  
[<span data-ttu-id="8e5b6-122">IMAPITable::GetLastError</span><span class="sxs-lookup"><span data-stu-id="8e5b6-122">IMAPITable::GetLastError</span></span>](imapitable-getlasterror.md)
  
[<span data-ttu-id="8e5b6-123">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="8e5b6-123">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="8e5b6-124">IMAPIViewAdviseSink::OnPrint</span><span class="sxs-lookup"><span data-stu-id="8e5b6-124">IMAPIViewAdviseSink::OnPrint</span></span>](imapiviewadvisesink-onprint.md)
  
## <a name="see-also"></a><span data-ttu-id="8e5b6-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="8e5b6-125">See also</span></span>



[<span data-ttu-id="8e5b6-126">SCODE</span><span class="sxs-lookup"><span data-stu-id="8e5b6-126">SCODE</span></span>](scode.md)


[<span data-ttu-id="8e5b6-127">MAPI のデータ型</span><span class="sxs-lookup"><span data-stu-id="8e5b6-127">MAPI Data Types</span></span>](mapi-data-types.md)

