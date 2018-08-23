---
title: SCODE
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
ms.assetid: 2348cce1-07c3-49ed-ae03-79e477d3c6c2
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 7f8ede3761ca10589c686e2ec4fac18fbe00fb2c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588588"
---
# <a name="scode"></a><span data-ttu-id="fe64d-103">SCODE</span><span class="sxs-lookup"><span data-stu-id="fe64d-103">SCODE</span></span>

<span data-ttu-id="fe64d-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fe64d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fe64d-105">エラーまたは警告を記述するために使用される 32 ビットのステータス値です。</span><span class="sxs-lookup"><span data-stu-id="fe64d-105">A 32-bit status value that is used to describe an error or warning.</span></span> 
  
```cpp
typedef ULONG SCODE;

```

## <a name="remarks"></a><span data-ttu-id="fe64d-106">注釈</span><span class="sxs-lookup"><span data-stu-id="fe64d-106">Remarks</span></span>

<span data-ttu-id="fe64d-107">**データは、 [HRESULT](hresult.md)のデータ型と同じです。**</span><span class="sxs-lookup"><span data-stu-id="fe64d-107">The **SCODE** data type is the same as the [HRESULT](hresult.md) data type.</span></span> 
  
<span data-ttu-id="fe64d-108">**SCODE**の値は、4 つのフィールドに分かれています。</span><span class="sxs-lookup"><span data-stu-id="fe64d-108">An **SCODE** value is divided into four fields:</span></span> 
  
- <span data-ttu-id="fe64d-109">返し、失敗を示すために 1 を 0 に設定されている単一のビットの重要度コードです。</span><span class="sxs-lookup"><span data-stu-id="fe64d-109">A single-bit severity code which is set to 0 to indicate success and 1 to indicate failure.</span></span>
    
- <span data-ttu-id="fe64d-110">11 ビットの予約フィールド</span><span class="sxs-lookup"><span data-stu-id="fe64d-110">An 11-bit reserved field</span></span>
    
- <span data-ttu-id="fe64d-111">領域エラーまたは警告を担当することを示す 4 ビットの機能のコードです。</span><span class="sxs-lookup"><span data-stu-id="fe64d-111">A 4-bit facility code which indicates the area responsible for the error or warning.</span></span>
    
- <span data-ttu-id="fe64d-112">16 ビットのエラーまたは警告コード エラーまたは警告は、問題について説明します。</span><span class="sxs-lookup"><span data-stu-id="fe64d-112">A 16-bit error or warning code which describes the problem that is causing the error or warning.</span></span>
    
<span data-ttu-id="fe64d-113">MAPI の関数およびメソッドの多くは、OLE メソッドと関数のように、 **HRESULT**のデータ型として定義されている**SCODE**の値を返します。</span><span class="sxs-lookup"><span data-stu-id="fe64d-113">Many of the MAPI functions and methods return **SCODE** values defined as **HRESULT** data types as do the OLE methods and functions.</span></span> <span data-ttu-id="fe64d-114">OLE は、 **SCODE**と**HRESULT**間の変換に使用できるいくつかのマクロを定義します。</span><span class="sxs-lookup"><span data-stu-id="fe64d-114">OLE defines several macros that can be used to convert between an **SCODE** and an **HRESULT**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="fe64d-115">64 ビットの MAPI で**られません**が、32 ビット値です。</span><span class="sxs-lookup"><span data-stu-id="fe64d-115">In 64-bit MAPI, **SCODE** is still a 32-bit value.</span></span> 
  
<span data-ttu-id="fe64d-116">MAPI が**SCODE**のデータ型を使用する方法の詳細については、[エラー処理](error-handling-in-mapi.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fe64d-116">For more information about how MAPI uses the **SCODE** data type, see [Error Handling](error-handling-in-mapi.md).</span></span> <span data-ttu-id="fe64d-117">OLE および**SCODE**のデータ型の詳細については、 *OLE プログラマ リファレンス*を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fe64d-117">For more information about OLE and the **SCODE** data type, see the  *OLE Programmer's Reference*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fe64d-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="fe64d-118">See also</span></span>



[<span data-ttu-id="fe64d-119">HRESULT 型</span><span class="sxs-lookup"><span data-stu-id="fe64d-119">HRESULT</span></span>](hresult.md)


[<span data-ttu-id="fe64d-120">MAPI データ型</span><span class="sxs-lookup"><span data-stu-id="fe64d-120">MAPI Data Types</span></span>](mapi-data-types.md)

