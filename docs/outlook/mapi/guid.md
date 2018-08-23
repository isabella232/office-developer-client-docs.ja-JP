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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 94bafdf0ca84fa31a7df2f022265d5d5d1a99a37
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577696"
---
# <a name="guid"></a><span data-ttu-id="e51f9-103">GUID</span><span class="sxs-lookup"><span data-stu-id="e51f9-103">GUID</span></span>

  
  
<span data-ttu-id="e51f9-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e51f9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e51f9-105">グローバル一意識別子 (GUID) をについて説明します。</span><span class="sxs-lookup"><span data-stu-id="e51f9-105">Describes a globally unique identifier (GUID).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e51f9-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="e51f9-106">Header file:</span></span>  <br/> |<span data-ttu-id="e51f9-107">Mapiguid.h</span><span class="sxs-lookup"><span data-stu-id="e51f9-107">Mapiguid.h</span></span>  <br/> |
   
```cpp
typedef struct _GUID
{
  unsigned long Data1;
  unsigned short Data2;
  unsigned short Data3;
  unsigned char Data4[8];
} GUID;

```

## <a name="members"></a><span data-ttu-id="e51f9-108">Members</span><span class="sxs-lookup"><span data-stu-id="e51f9-108">Members</span></span>

 <span data-ttu-id="e51f9-109">**Data1**</span><span class="sxs-lookup"><span data-stu-id="e51f9-109">**Data1**</span></span>
  
> <span data-ttu-id="e51f9-110">符号なし長整数型のデータの値の場合です。</span><span class="sxs-lookup"><span data-stu-id="e51f9-110">An unsigned long integer data value.</span></span>
    
 <span data-ttu-id="e51f9-111">**Data2**</span><span class="sxs-lookup"><span data-stu-id="e51f9-111">**Data2**</span></span>
  
> <span data-ttu-id="e51f9-112">符号なし短整数データの値。</span><span class="sxs-lookup"><span data-stu-id="e51f9-112">An unsigned short integer data value.</span></span>
    
 <span data-ttu-id="e51f9-113">**Data3**</span><span class="sxs-lookup"><span data-stu-id="e51f9-113">**Data3**</span></span>
  
> <span data-ttu-id="e51f9-114">符号なし短整数データの値。</span><span class="sxs-lookup"><span data-stu-id="e51f9-114">An unsigned short integer data value.</span></span>
    
 <span data-ttu-id="e51f9-115">**Data4**</span><span class="sxs-lookup"><span data-stu-id="e51f9-115">**Data4**</span></span>
  
> <span data-ttu-id="e51f9-116">符号なしの文字の配列。</span><span class="sxs-lookup"><span data-stu-id="e51f9-116">An array of unsigned characters.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e51f9-117">注釈</span><span class="sxs-lookup"><span data-stu-id="e51f9-117">Remarks</span></span>

 <span data-ttu-id="e51f9-118">**GUID**構造体は、次のようの MAPI で使用されます。</span><span class="sxs-lookup"><span data-stu-id="e51f9-118">**GUID** structures are used in MAPI as follows:</span></span> 
  
- <span data-ttu-id="e51f9-119">[MAPIUID](mapiuid.md)構造体でサービス プロバイダーを一意に識別します。</span><span class="sxs-lookup"><span data-stu-id="e51f9-119">In the [MAPIUID](mapiuid.md) structures that uniquely identify service providers.</span></span> 
    
- <span data-ttu-id="e51f9-120">インターフェイス識別子です。</span><span class="sxs-lookup"><span data-stu-id="e51f9-120">For interface identifiers.</span></span>
    
- <span data-ttu-id="e51f9-121">プロパティには、名前付きプロパティの名前を設定します。</span><span class="sxs-lookup"><span data-stu-id="e51f9-121">In the property set names of named properties.</span></span> 
    
<span data-ttu-id="e51f9-122">メッセージ ストアとアドレス帳プロバイダーは、 **MAPIUID**構造体で使用する**GUID**構造体を生成します。</span><span class="sxs-lookup"><span data-stu-id="e51f9-122">Message store and address book providers generate a **GUID** structure to use in their **MAPIUID** structure.</span></span> <span data-ttu-id="e51f9-123">結果として得られる**MAPIUID**を[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)に渡すことによっては、これらのサービス プロバイダーは、その一意の識別子の MAPI を通知します。</span><span class="sxs-lookup"><span data-stu-id="e51f9-123">By passing the resulting **MAPIUID** to [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md), these service providers inform MAPI of their unique identifier.</span></span>
  
<span data-ttu-id="e51f9-124">また、Microsoft リモート プロシージャ コール (RPC) およびオブジェクトの説明言語 (ODL) の実装に使用されます。</span><span class="sxs-lookup"><span data-stu-id="e51f9-124">Also, they are used in the implementation of Microsoft Remote Procedure Call (RPC) and the Object Description Language (ODL).</span></span> <span data-ttu-id="e51f9-125">これらの使用の詳細については、の*Microsoft RPC プログラマーズ ガイドと参照*、 *OLE プログラマ リファレンス*、および*内部 OLE*、*第 2 版*を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e51f9-125">For more information about these uses, see the  *Microsoft RPC Programmer's Guide and Reference*, *OLE Programmer's Reference*  ,and  *Inside OLE*, *Second Edition*  .</span></span> 
  
<span data-ttu-id="e51f9-126">**GUID**構造体は、 *Win32 プログラマーズ リファレンス*で定義されます。</span><span class="sxs-lookup"><span data-stu-id="e51f9-126">The **GUID** structure is defined in the  *Win32 Programmer's Reference*  .</span></span> <span data-ttu-id="e51f9-127">MAPI ヘッダー ファイル Mapiguid.h には、MAPI 内で使用する**GUID**構造体の特定の値が定義されています。</span><span class="sxs-lookup"><span data-stu-id="e51f9-127">Specific values for **GUID** structures that are used within MAPI are defined in the MAPI header file Mapiguid.h.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e51f9-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="e51f9-128">See also</span></span>



[<span data-ttu-id="e51f9-129">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="e51f9-129">MAPIUID</span></span>](mapiuid.md)


[<span data-ttu-id="e51f9-130">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="e51f9-130">MAPI Structures</span></span>](mapi-structures.md)

