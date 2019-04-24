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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 4208f51af44055b03c65b51c9b3d94e947dc9b68
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351241"
---
# <a name="scode"></a><span data-ttu-id="cbee0-103">SCODE</span><span class="sxs-lookup"><span data-stu-id="cbee0-103">SCODE</span></span>

<span data-ttu-id="cbee0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cbee0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cbee0-105">エラーまたは警告を記述するために使用される32ビットの状態の値。</span><span class="sxs-lookup"><span data-stu-id="cbee0-105">A 32-bit status value that is used to describe an error or warning.</span></span> 
  
```cpp
typedef ULONG SCODE;

```

## <a name="remarks"></a><span data-ttu-id="cbee0-106">解説</span><span class="sxs-lookup"><span data-stu-id="cbee0-106">Remarks</span></span>

<span data-ttu-id="cbee0-107">**SCODE**データ型は、 [HRESULT](hresult.md)データ型と同じです。</span><span class="sxs-lookup"><span data-stu-id="cbee0-107">The **SCODE** data type is the same as the [HRESULT](hresult.md) data type.</span></span> 
  
<span data-ttu-id="cbee0-108">**SCODE**値は、次の4つのフィールドに分かれています。</span><span class="sxs-lookup"><span data-stu-id="cbee0-108">An **SCODE** value is divided into four fields:</span></span> 
  
- <span data-ttu-id="cbee0-109">成功を示す0に設定されている1ビットの重大度コード。エラーを示す1を指定します。</span><span class="sxs-lookup"><span data-stu-id="cbee0-109">A single-bit severity code which is set to 0 to indicate success and 1 to indicate failure.</span></span>
    
- <span data-ttu-id="cbee0-110">11ビットの予約済みフィールド</span><span class="sxs-lookup"><span data-stu-id="cbee0-110">An 11-bit reserved field</span></span>
    
- <span data-ttu-id="cbee0-111">エラーまたは警告を担当する領域を示す4ビットのファシリティコード。</span><span class="sxs-lookup"><span data-stu-id="cbee0-111">A 4-bit facility code which indicates the area responsible for the error or warning.</span></span>
    
- <span data-ttu-id="cbee0-112">エラーまたは警告を引き起こしている問題を説明する16ビットエラーまたは警告コード。</span><span class="sxs-lookup"><span data-stu-id="cbee0-112">A 16-bit error or warning code which describes the problem that is causing the error or warning.</span></span>
    
<span data-ttu-id="cbee0-113">多くの MAPI の関数およびメソッドは、OLE のメソッドと関数として、 **HRESULT**データ型として定義された**SCODE**値を返します。</span><span class="sxs-lookup"><span data-stu-id="cbee0-113">Many of the MAPI functions and methods return **SCODE** values defined as **HRESULT** data types as do the OLE methods and functions.</span></span> <span data-ttu-id="cbee0-114">OLE は、 **SCODE**と**HRESULT**の間の変換に使用できるいくつかのマクロを定義します。</span><span class="sxs-lookup"><span data-stu-id="cbee0-114">OLE defines several macros that can be used to convert between an **SCODE** and an **HRESULT**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="cbee0-115">64ビット MAPI では、 **SCODE**は32ビット値のままです。</span><span class="sxs-lookup"><span data-stu-id="cbee0-115">In 64-bit MAPI, **SCODE** is still a 32-bit value.</span></span> 
  
<span data-ttu-id="cbee0-116">MAPI が**SCODE**データ型を使用する方法の詳細については、「[エラー処理](error-handling-in-mapi.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cbee0-116">For more information about how MAPI uses the **SCODE** data type, see [Error Handling](error-handling-in-mapi.md).</span></span> <span data-ttu-id="cbee0-117">ole および**SCODE**データ型の詳細については、「 *ole プログラマーズリファレンス*」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cbee0-117">For more information about OLE and the **SCODE** data type, see the  *OLE Programmer's Reference*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cbee0-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="cbee0-118">See also</span></span>



[<span data-ttu-id="cbee0-119">HRESULT 型</span><span class="sxs-lookup"><span data-stu-id="cbee0-119">HRESULT</span></span>](hresult.md)


[<span data-ttu-id="cbee0-120">MAPI のデータ型</span><span class="sxs-lookup"><span data-stu-id="cbee0-120">MAPI Data Types</span></span>](mapi-data-types.md)

