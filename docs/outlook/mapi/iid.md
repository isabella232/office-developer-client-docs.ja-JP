---
title: IID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.IID
api_type:
- COM
ms.assetid: fa5498ab-2f8a-42f8-ba9d-1d555768594f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 5605de7dbcc18197748713bcf909839690d7259f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336352"
---
# <a name="iid"></a><span data-ttu-id="90a6e-103">IID</span><span class="sxs-lookup"><span data-stu-id="90a6e-103">IID</span></span>

  
  
<span data-ttu-id="90a6e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="90a6e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="90a6e-105">MAPI インターフェイスの識別子を記述するために使用される[GUID](guid.md)構造を記述します。</span><span class="sxs-lookup"><span data-stu-id="90a6e-105">Describes a [GUID](guid.md) structure used to describe an identifier for a MAPI interface.</span></span> 
  
```cpp
typedef struct _GUID
{
  unsigned long Data1;
  unsigned short Data2;
  unsigned short Data3;
  unsigned char Data4[8];
} GUID;

```

## <a name="members"></a><span data-ttu-id="90a6e-106">Members</span><span class="sxs-lookup"><span data-stu-id="90a6e-106">Members</span></span>

<span data-ttu-id="90a6e-107">**GUID**構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="90a6e-107">See the **GUID** structure.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="90a6e-108">解説</span><span class="sxs-lookup"><span data-stu-id="90a6e-108">Remarks</span></span>

<span data-ttu-id="90a6e-109">**IID**構造は、MAPI インターフェイスを一意に識別し、特定のインターフェイスをオブジェクトに関連付けるために使用されます。</span><span class="sxs-lookup"><span data-stu-id="90a6e-109">An **IID** structure is used to uniquely identify a MAPI interface and to associate a particular interface with an object.</span></span> <span data-ttu-id="90a6e-110">たとえば、クライアントが[imapisession:: openentry](imapisession-openentry.md)を呼び出してフォルダーを開くと、クライアントは[imapisession](imapifolderimapicontainer.md)インターフェイスを表す**IID**を指すように_lpinterface_パラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="90a6e-110">For example, when a client calls [IMAPISession::OpenEntry](imapisession-openentry.md) to open a folder, the client sets the  _lpInterface_ parameter to point to an **IID** representing the [IMAPIFolder](imapifolderimapicontainer.md) interface.</span></span> <span data-ttu-id="90a6e-111">MAPI は、IID_IMAPIFolder する**IMAPIFolderIID**を定義します。</span><span class="sxs-lookup"><span data-stu-id="90a6e-111">MAPI defines the **IMAPIFolderIID** to be IID_IMAPIFolder.</span></span> <span data-ttu-id="90a6e-112">**IID**の構造体は、OLE インターフェイスを一意に識別するためにも使用されます。</span><span class="sxs-lookup"><span data-stu-id="90a6e-112">**IID** structures are also used to uniquely identify OLE interfaces.</span></span> 
  
<span data-ttu-id="90a6e-113">MAPI インターフェイスの特定の**IID**構造はすべて、mapiguid .h ヘッダーファイルで定義されています。</span><span class="sxs-lookup"><span data-stu-id="90a6e-113">All of the specific **IID** structures for the MAPI interfaces are defined in the Mapiguid.h header file.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="90a6e-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="90a6e-114">See also</span></span>



[<span data-ttu-id="90a6e-115">GUID</span><span class="sxs-lookup"><span data-stu-id="90a6e-115">GUID</span></span>](guid.md)


[<span data-ttu-id="90a6e-116">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="90a6e-116">MAPI Structures</span></span>](mapi-structures.md)

