---
title: TCHAR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
api_name:
- MAPI.TCHAR
api_type:
- COM
ms.assetid: 7a92060b-4c30-4eba-993f-36f5f9231a4b
description: '最終更新日: 2011 年 7 月 23 日'
localization_priority: Priority
ms.openlocfilehash: 2b04ebe6d05cd72a59fe6d44c9138468fd7ddec1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710448"
---
# <a name="tchar"></a><span data-ttu-id="80082-103">TCHAR</span><span class="sxs-lookup"><span data-stu-id="80082-103">TCHAR</span></span>

  
  
<span data-ttu-id="80082-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="80082-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="80082-105">ANSI、DBCS、または Unicode 文字列の記述に使用できる Win32 文字の文字列。</span><span class="sxs-lookup"><span data-stu-id="80082-105">A Win32 character string that can be used to describe ANSI, DBCS, or Unicode strings.</span></span> <span data-ttu-id="80082-106">ANSI および DBCS プラットフォームの場合、TCHAR は次のように定義されています。</span><span class="sxs-lookup"><span data-stu-id="80082-106">For ANSI and DBCS platforms, TCHAR is defined as follows:</span></span>
  
```cpp
typedef char TCHAR;

```

## <a name="remarks"></a><span data-ttu-id="80082-107">解説</span><span class="sxs-lookup"><span data-stu-id="80082-107">Remarks</span></span>

<span data-ttu-id="80082-108">Unicode プラットフォームの場合、TCHAR は WCHAR 型と同義語として定義されています。</span><span class="sxs-lookup"><span data-stu-id="80082-108">For Unicode platforms, TCHAR is defined as synonymous with the WCHAR type.</span></span> 
  
<span data-ttu-id="80082-109">MAPI のクライアントでは、TCHAR データ型を使用して WCHAR または char 型のいずれかの文字列を表すことができます。</span><span class="sxs-lookup"><span data-stu-id="80082-109">MAPI clients can use the TCHAR data type to represent a string of either the WCHAR or char type.</span></span> <span data-ttu-id="80082-110">シンボリック定数 UNICODE を定義し、必要に応じてプラットフォームを制限してください。</span><span class="sxs-lookup"><span data-stu-id="80082-110">Be sure to define the symbolic constant UNICODE and limit the platform when it is required.</span></span> <span data-ttu-id="80082-111">MAPI はプラットフォーム情報を解釈し、内部的に TCHAR を適切な文字列に変換します。</span><span class="sxs-lookup"><span data-stu-id="80082-111">MAPI will interpret the platform information and internally translate TCHAR to the appropriate string.</span></span> <span data-ttu-id="80082-112">MAPI のプロパティ型 (PT_TSTRING) は、TCHAR データ型と同様に機能します。</span><span class="sxs-lookup"><span data-stu-id="80082-112">The MAPI property type, PT_TSTRING, works just like the TCHAR data type.</span></span> <span data-ttu-id="80082-113">プラットフォームが Unicode をサポートしている場合は、コンパイル時に PT_UNICODE 型が PT_TSTRING 型のプロパティに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="80082-113">When the platform supports Unicode, properties of type PT_TSTRING are assigned the type PT_UNICODE at compile time.</span></span> <span data-ttu-id="80082-114">プラットフォームが Unicode をサポートしていない場合は、これらのプロパティに PT_STRING8 型が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="80082-114">When the platform does not support Unicode, these properties are assigned the type PT_STRING8.</span></span>
  
<span data-ttu-id="80082-115">この機能の詳細については、「[文字セット](mapi-character-sets.md)」および「[プロパティの型のリスト](property-types.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="80082-115">For more information about this functionality, see [Character Sets](mapi-character-sets.md) and [List of Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="80082-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="80082-116">See also</span></span>



[<span data-ttu-id="80082-117">MAPI のデータ型</span><span class="sxs-lookup"><span data-stu-id="80082-117">MAPI Data Types</span></span>](mapi-data-types.md)

