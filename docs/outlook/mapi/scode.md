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
ms.openlocfilehash: 6cd9dfe8fabd1ae7a4389550c628fb7ceff09ea8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803827"
---
# <a name="scode"></a><span data-ttu-id="658cb-103">SCODE</span><span class="sxs-lookup"><span data-stu-id="658cb-103">SCODE</span></span>

<span data-ttu-id="658cb-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="658cb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="658cb-105">エラーまたは警告を記述するために使用される 32 ビットのステータス値です。</span><span class="sxs-lookup"><span data-stu-id="658cb-105">A 32-bit status value that is used to describe an error or warning.</span></span> 
  
```cpp
typedef ULONG SCODE;

```

## <a name="remarks"></a><span data-ttu-id="658cb-106">備考</span><span class="sxs-lookup"><span data-stu-id="658cb-106">Remarks</span></span>

<span data-ttu-id="658cb-107">**データは、 [HRESULT](hresult.md)のデータ型と同じです。**</span><span class="sxs-lookup"><span data-stu-id="658cb-107">The **SCODE** data type is the same as the [HRESULT](hresult.md) data type.</span></span> 
  
<span data-ttu-id="658cb-108">**SCODE**の値は、4 つのフィールドに分かれています。</span><span class="sxs-lookup"><span data-stu-id="658cb-108">An **SCODE** value is divided into four fields:</span></span> 
  
- <span data-ttu-id="658cb-109">返し、失敗を示すために 1 を 0 に設定されている単一のビットの重要度コードです。</span><span class="sxs-lookup"><span data-stu-id="658cb-109">A single-bit severity code which is set to 0 to indicate success and 1 to indicate failure.</span></span>
    
- <span data-ttu-id="658cb-110">11 ビットの予約フィールド</span><span class="sxs-lookup"><span data-stu-id="658cb-110">An 11-bit reserved field</span></span>
    
- <span data-ttu-id="658cb-111">領域エラーまたは警告を担当することを示す 4 ビットの機能のコードです。</span><span class="sxs-lookup"><span data-stu-id="658cb-111">A 4-bit facility code which indicates the area responsible for the error or warning.</span></span>
    
- <span data-ttu-id="658cb-112">16 ビットのエラーまたは警告コード エラーまたは警告は、問題について説明します。</span><span class="sxs-lookup"><span data-stu-id="658cb-112">A 16-bit error or warning code which describes the problem that is causing the error or warning.</span></span>
    
<span data-ttu-id="658cb-113">MAPI の関数およびメソッドの多くは、OLE メソッドと関数のように、 **HRESULT**のデータ型として定義されている**SCODE**の値を返します。</span><span class="sxs-lookup"><span data-stu-id="658cb-113">Many of the MAPI functions and methods return **SCODE** values defined as **HRESULT** data types as do the OLE methods and functions.</span></span> <span data-ttu-id="658cb-114">OLE は、 **SCODE**と**HRESULT**間の変換に使用できるいくつかのマクロを定義します。</span><span class="sxs-lookup"><span data-stu-id="658cb-114">OLE defines several macros that can be used to convert between an **SCODE** and an **HRESULT**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="658cb-115">64 ビットの MAPI で**られません**が、32 ビット値です。</span><span class="sxs-lookup"><span data-stu-id="658cb-115">In 64-bit MAPI, **SCODE** is still a 32-bit value.</span></span> 
  
<span data-ttu-id="658cb-116">MAPI が**SCODE**のデータ型を使用する方法の詳細については、[エラー処理](error-handling-in-mapi.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="658cb-116">For more information about how MAPI uses the **SCODE** data type, see [Error Handling](error-handling-in-mapi.md).</span></span> <span data-ttu-id="658cb-117">OLE および**SCODE**のデータ型の詳細については、 *OLE プログラマ リファレンス*を参照してください。</span><span class="sxs-lookup"><span data-stu-id="658cb-117">For more information about OLE and the **SCODE** data type, see the  *OLE Programmer's Reference*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="658cb-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="658cb-118">See also</span></span>



[<span data-ttu-id="658cb-119">HRESULT 型</span><span class="sxs-lookup"><span data-stu-id="658cb-119">HRESULT</span></span>](hresult.md)


[<span data-ttu-id="658cb-120">MAPI データ型</span><span class="sxs-lookup"><span data-stu-id="658cb-120">MAPI Data Types</span></span>](mapi-data-types.md)

