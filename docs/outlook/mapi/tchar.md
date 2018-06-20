---
title: TCHAR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.TCHAR
api_type:
- COM
ms.assetid: 7a92060b-4c30-4eba-993f-36f5f9231a4b
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: e7b3774d8dce446f0e87f041f11dac607f464680
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804102"
---
# <a name="tchar"></a><span data-ttu-id="b4fb5-103">TCHAR</span><span class="sxs-lookup"><span data-stu-id="b4fb5-103">TCHAR</span></span>

  
  
<span data-ttu-id="b4fb5-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b4fb5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b4fb5-105">ANSI、DBCS、または Unicode の文字列を記述するために使用する Win32 文字の文字列です。</span><span class="sxs-lookup"><span data-stu-id="b4fb5-105">A Win32 character string that can be used to describe ANSI, DBCS, or Unicode strings.</span></span> <span data-ttu-id="b4fb5-106">ANSI と DBCS のプラットフォームの TCHAR は次のように定義されます。</span><span class="sxs-lookup"><span data-stu-id="b4fb5-106">For ANSI and DBCS platforms, TCHAR is defined as follows:</span></span>
  
```cpp
typedef char TCHAR;

```

## <a name="remarks"></a><span data-ttu-id="b4fb5-107">備考</span><span class="sxs-lookup"><span data-stu-id="b4fb5-107">Remarks</span></span>

<span data-ttu-id="b4fb5-108">Unicode プラットフォームの場合は、TCHAR は WCHAR 型と同じ意味として定義されます。</span><span class="sxs-lookup"><span data-stu-id="b4fb5-108">For Unicode platforms, TCHAR is defined as synonymous with the WCHAR type.</span></span> 
  
<span data-ttu-id="b4fb5-109">MAPI クライアントでは、WCHAR または char 型の文字列を表すため、TCHAR データ型を使用できます。</span><span class="sxs-lookup"><span data-stu-id="b4fb5-109">MAPI clients can use the TCHAR data type to represent a string of either the WCHAR or char type.</span></span> <span data-ttu-id="b4fb5-110">シンボリック定数の UNICODE を定義し、必要な場合に、プラットフォームを制限することを確認します。</span><span class="sxs-lookup"><span data-stu-id="b4fb5-110">Be sure to define the symbolic constant UNICODE and limit the platform when it is required.</span></span> <span data-ttu-id="b4fb5-111">MAPI はプラットフォームの情報を解釈し、内部的に TCHAR を適切な文字列に変換します。</span><span class="sxs-lookup"><span data-stu-id="b4fb5-111">MAPI will interpret the platform information and internally translate TCHAR to the appropriate string.</span></span> <span data-ttu-id="b4fb5-112">MAPI プロパティの型、PT_TSTRING は、TCHAR データ型と同じように動作します。</span><span class="sxs-lookup"><span data-stu-id="b4fb5-112">The MAPI property type, PT_TSTRING, works just like the TCHAR data type.</span></span> <span data-ttu-id="b4fb5-113">プラットフォームでは、Unicode をサポートする PT_TSTRING の種類のプロパティはコンパイル時に PT_UNICODE の種類に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="b4fb5-113">When the platform supports Unicode, properties of type PT_TSTRING are assigned the type PT_UNICODE at compile time.</span></span> <span data-ttu-id="b4fb5-114">プラットフォームでは、Unicode をサポートしていない、これらのプロパティに PT_STRING8 の種類が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="b4fb5-114">When the platform does not support Unicode, these properties are assigned the type PT_STRING8.</span></span>
  
<span data-ttu-id="b4fb5-115">この機能の詳細については、[文字セット](mapi-character-sets.md)と[プロパティの種類の一覧](property-types.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b4fb5-115">For more information about this functionality, see [Character Sets](mapi-character-sets.md) and [List of Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b4fb5-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="b4fb5-116">See also</span></span>



[<span data-ttu-id="b4fb5-117">MAPI データ型</span><span class="sxs-lookup"><span data-stu-id="b4fb5-117">MAPI Data Types</span></span>](mapi-data-types.md)

