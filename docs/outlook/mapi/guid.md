---
title: GUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.GUID
api_type:
- COM
ms.assetid: e3608c47-06be-4476-a6ef-060fac252387
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 12c50ab5936d7fffd364c276ba07ca69d3459ae7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421586"
---
# <a name="guid"></a><span data-ttu-id="90e43-103">GUID</span><span class="sxs-lookup"><span data-stu-id="90e43-103">GUID</span></span>

  
  
<span data-ttu-id="90e43-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="90e43-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="90e43-105">グローバル一意識別子 (GUID) について説明します。</span><span class="sxs-lookup"><span data-stu-id="90e43-105">Describes a globally unique identifier (GUID).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="90e43-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="90e43-106">Header file:</span></span>  <br/> |<span data-ttu-id="90e43-107">Mapiguid.h</span><span class="sxs-lookup"><span data-stu-id="90e43-107">Mapiguid.h</span></span>  <br/> |
   
```cpp
typedef struct _GUID
{
  unsigned long Data1;
  unsigned short Data2;
  unsigned short Data3;
  unsigned char Data4[8];
} GUID;

```

## <a name="members"></a><span data-ttu-id="90e43-108">Members</span><span class="sxs-lookup"><span data-stu-id="90e43-108">Members</span></span>

 <span data-ttu-id="90e43-109">**Data1**</span><span class="sxs-lookup"><span data-stu-id="90e43-109">**Data1**</span></span>
  
> <span data-ttu-id="90e43-110">符号なし長整数データ値。</span><span class="sxs-lookup"><span data-stu-id="90e43-110">An unsigned long integer data value.</span></span>
    
 <span data-ttu-id="90e43-111">**Data2**</span><span class="sxs-lookup"><span data-stu-id="90e43-111">**Data2**</span></span>
  
> <span data-ttu-id="90e43-112">符号なし短整数データ値。</span><span class="sxs-lookup"><span data-stu-id="90e43-112">An unsigned short integer data value.</span></span>
    
 <span data-ttu-id="90e43-113">**Data3**</span><span class="sxs-lookup"><span data-stu-id="90e43-113">**Data3**</span></span>
  
> <span data-ttu-id="90e43-114">符号なし短整数データ値。</span><span class="sxs-lookup"><span data-stu-id="90e43-114">An unsigned short integer data value.</span></span>
    
 <span data-ttu-id="90e43-115">**Data4**</span><span class="sxs-lookup"><span data-stu-id="90e43-115">**Data4**</span></span>
  
> <span data-ttu-id="90e43-116">符号なし文字の配列。</span><span class="sxs-lookup"><span data-stu-id="90e43-116">An array of unsigned characters.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="90e43-117">注釈</span><span class="sxs-lookup"><span data-stu-id="90e43-117">Remarks</span></span>

 <span data-ttu-id="90e43-118">**GUID** 構造は、次のように MAPI で使用されます。</span><span class="sxs-lookup"><span data-stu-id="90e43-118">**GUID** structures are used in MAPI as follows:</span></span> 
  
- <span data-ttu-id="90e43-119">サービス プロバイダーを一意に識別する [MAPIUID](mapiuid.md) 構造。</span><span class="sxs-lookup"><span data-stu-id="90e43-119">In the [MAPIUID](mapiuid.md) structures that uniquely identify service providers.</span></span> 
    
- <span data-ttu-id="90e43-120">インターフェイス識別子の場合。</span><span class="sxs-lookup"><span data-stu-id="90e43-120">For interface identifiers.</span></span>
    
- <span data-ttu-id="90e43-121">プロパティで、名前付きプロパティの名前を設定します。</span><span class="sxs-lookup"><span data-stu-id="90e43-121">In the property set names of named properties.</span></span> 
    
<span data-ttu-id="90e43-122">メッセージ ストアとアドレス帳プロバイダーは **、MAPIUID** 構造で使用する **GUID 構造を生成** します。</span><span class="sxs-lookup"><span data-stu-id="90e43-122">Message store and address book providers generate a **GUID** structure to use in their **MAPIUID** structure.</span></span> <span data-ttu-id="90e43-123">結果の **MAPIUID** を [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)に渡して、これらのサービス プロバイダーは MAPI に一意の識別子を通知します。</span><span class="sxs-lookup"><span data-stu-id="90e43-123">By passing the resulting **MAPIUID** to [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md), these service providers inform MAPI of their unique identifier.</span></span>
  
<span data-ttu-id="90e43-124">また、Microsoft リモート プロシージャ 呼び出し (RPC) およびオブジェクト記述言語 (ODL) の実装でも使用されます。</span><span class="sxs-lookup"><span data-stu-id="90e43-124">Also, they are used in the implementation of Microsoft Remote Procedure Call (RPC) and the Object Description Language (ODL).</span></span> <span data-ttu-id="90e43-125">これらの使用の詳細については *、「Microsoft RPC プログラマ* ガイドとリファレンス」、OLEプログラマリファレンス *、Inside OLE 、Second* Edition を *参照してください*。</span><span class="sxs-lookup"><span data-stu-id="90e43-125">For more information about these uses, see the  *Microsoft RPC Programmer's Guide and Reference*, *OLE Programmer's Reference*  ,and  *Inside OLE*, *Second Edition*  .</span></span> 
  
<span data-ttu-id="90e43-126">**GUID 構造** は *、Win32 プログラマリファレンスで定義されています*。</span><span class="sxs-lookup"><span data-stu-id="90e43-126">The **GUID** structure is defined in the  *Win32 Programmer's Reference*  .</span></span> <span data-ttu-id="90e43-127">MAPI 内で **使用される GUID** 構造体の特定の値は、MAPI ヘッダー ファイル Mapiguid.h で定義されます。</span><span class="sxs-lookup"><span data-stu-id="90e43-127">Specific values for **GUID** structures that are used within MAPI are defined in the MAPI header file Mapiguid.h.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="90e43-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="90e43-128">See also</span></span>



[<span data-ttu-id="90e43-129">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="90e43-129">MAPIUID</span></span>](mapiuid.md)


[<span data-ttu-id="90e43-130">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="90e43-130">MAPI Structures</span></span>](mapi-structures.md)

