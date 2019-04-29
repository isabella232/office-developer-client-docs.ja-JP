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
# <a name="guid"></a><span data-ttu-id="0028f-103">GUID</span><span class="sxs-lookup"><span data-stu-id="0028f-103">GUID</span></span>

  
  
<span data-ttu-id="0028f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0028f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0028f-105">グローバル一意識別子 (GUID) を記述します。</span><span class="sxs-lookup"><span data-stu-id="0028f-105">Describes a globally unique identifier (GUID).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0028f-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="0028f-106">Header file:</span></span>  <br/> |<span data-ttu-id="0028f-107">mapiguid. .h</span><span class="sxs-lookup"><span data-stu-id="0028f-107">Mapiguid.h</span></span>  <br/> |
   
```cpp
typedef struct _GUID
{
  unsigned long Data1;
  unsigned short Data2;
  unsigned short Data3;
  unsigned char Data4[8];
} GUID;

```

## <a name="members"></a><span data-ttu-id="0028f-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="0028f-108">Members</span></span>

 <span data-ttu-id="0028f-109">**Data1**</span><span class="sxs-lookup"><span data-stu-id="0028f-109">**Data1**</span></span>
  
> <span data-ttu-id="0028f-110">符号なしの長整数型 (long) のデータ値。</span><span class="sxs-lookup"><span data-stu-id="0028f-110">An unsigned long integer data value.</span></span>
    
 <span data-ttu-id="0028f-111">**Data2**</span><span class="sxs-lookup"><span data-stu-id="0028f-111">**Data2**</span></span>
  
> <span data-ttu-id="0028f-112">符号なし short 整数型のデータ値。</span><span class="sxs-lookup"><span data-stu-id="0028f-112">An unsigned short integer data value.</span></span>
    
 <span data-ttu-id="0028f-113">**Data3**</span><span class="sxs-lookup"><span data-stu-id="0028f-113">**Data3**</span></span>
  
> <span data-ttu-id="0028f-114">符号なし short 整数型のデータ値。</span><span class="sxs-lookup"><span data-stu-id="0028f-114">An unsigned short integer data value.</span></span>
    
 <span data-ttu-id="0028f-115">**Data4**</span><span class="sxs-lookup"><span data-stu-id="0028f-115">**Data4**</span></span>
  
> <span data-ttu-id="0028f-116">符号なしの文字の配列。</span><span class="sxs-lookup"><span data-stu-id="0028f-116">An array of unsigned characters.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0028f-117">注釈</span><span class="sxs-lookup"><span data-stu-id="0028f-117">Remarks</span></span>

 <span data-ttu-id="0028f-118">**GUID**構造は、次のように MAPI で使用されます。</span><span class="sxs-lookup"><span data-stu-id="0028f-118">**GUID** structures are used in MAPI as follows:</span></span> 
  
- <span data-ttu-id="0028f-119">[MAPIUID](mapiuid.md)構造で、サービスプロバイダーを一意に識別します。</span><span class="sxs-lookup"><span data-stu-id="0028f-119">In the [MAPIUID](mapiuid.md) structures that uniquely identify service providers.</span></span> 
    
- <span data-ttu-id="0028f-120">インターフェイス識別子の場合。</span><span class="sxs-lookup"><span data-stu-id="0028f-120">For interface identifiers.</span></span>
    
- <span data-ttu-id="0028f-121">プロパティの名前付きプロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="0028f-121">In the property set names of named properties.</span></span> 
    
<span data-ttu-id="0028f-122">メッセージストアプロバイダーとアドレス帳プロバイダーは、 **MAPIUID**構造で使用する**GUID**構造を生成します。</span><span class="sxs-lookup"><span data-stu-id="0028f-122">Message store and address book providers generate a **GUID** structure to use in their **MAPIUID** structure.</span></span> <span data-ttu-id="0028f-123">結果の**MAPIUID**を[imapisupport:: setprovideruid](imapisupport-setprovideruid.md)に渡すことにより、これらのサービスプロバイダーは、一意の識別子を MAPI に通知します。</span><span class="sxs-lookup"><span data-stu-id="0028f-123">By passing the resulting **MAPIUID** to [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md), these service providers inform MAPI of their unique identifier.</span></span>
  
<span data-ttu-id="0028f-124">また、Microsoft リモートプロシージャコール (RPC) およびオブジェクト記述言語 (ODL) の実装でも使用されます。</span><span class="sxs-lookup"><span data-stu-id="0028f-124">Also, they are used in the implementation of Microsoft Remote Procedure Call (RPC) and the Object Description Language (ODL).</span></span> <span data-ttu-id="0028f-125">これらの使用の詳細については、「 *Microsoft RPC プログラマーズガイドとリファレンス*」、「 *ole プログラマーズリファレンス*」、および「 *ole*、 *Second Edition* 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0028f-125">For more information about these uses, see the  *Microsoft RPC Programmer's Guide and Reference*, *OLE Programmer's Reference*  ,and  *Inside OLE*, *Second Edition*  .</span></span> 
  
<span data-ttu-id="0028f-126">**GUID**構造は、 *Win32 プログラマーズリファレンス*で定義されています。</span><span class="sxs-lookup"><span data-stu-id="0028f-126">The **GUID** structure is defined in the  *Win32 Programmer's Reference*  .</span></span> <span data-ttu-id="0028f-127">mapi 内で使用される**GUID**構造の特定の値は、mapi ヘッダーファイルの mapiguid で定義されます。</span><span class="sxs-lookup"><span data-stu-id="0028f-127">Specific values for **GUID** structures that are used within MAPI are defined in the MAPI header file Mapiguid.h.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0028f-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="0028f-128">See also</span></span>



[<span data-ttu-id="0028f-129">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="0028f-129">MAPIUID</span></span>](mapiuid.md)


[<span data-ttu-id="0028f-130">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="0028f-130">MAPI Structures</span></span>](mapi-structures.md)

