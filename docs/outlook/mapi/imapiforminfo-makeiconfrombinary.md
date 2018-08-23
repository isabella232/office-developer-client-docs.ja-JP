---
title: IMAPIFormInfoMakeIconFromBinary
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.MakeIconFromBinary
api_type:
- COM
ms.assetid: 4daeddd7-3f0c-4178-ae8d-f74814090d40
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 30f55044327eecee3ab0d8ee2509d7132ab6e8ee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570129"
---
# <a name="imapiforminfomakeiconfrombinary"></a><span data-ttu-id="9b750-103">IMAPIFormInfo::MakeIconFromBinary</span><span class="sxs-lookup"><span data-stu-id="9b750-103">IMAPIFormInfo::MakeIconFromBinary</span></span>

  
  
<span data-ttu-id="9b750-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b750-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9b750-105">フォームのアイコンのプロパティのいずれかからアイコンを作成します。</span><span class="sxs-lookup"><span data-stu-id="9b750-105">Builds an icon from one of the icon properties of a form.</span></span>
  
```cpp
HRESULT MakeIconFromBinary(
  ULONG nPropID,
  HICON FAR * phicon
);
```

## <a name="parameters"></a><span data-ttu-id="9b750-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9b750-106">Parameters</span></span>

 <span data-ttu-id="9b750-107">_nPropID_</span><span class="sxs-lookup"><span data-stu-id="9b750-107">_nPropID_</span></span>
  
> <span data-ttu-id="9b750-108">[in]アイコンのプロパティにプロパティの識別子です。</span><span class="sxs-lookup"><span data-stu-id="9b750-108">[in] A property identifier for an icon property.</span></span>
    
 <span data-ttu-id="9b750-109">_phicon_</span><span class="sxs-lookup"><span data-stu-id="9b750-109">_phicon_</span></span>
  
> <span data-ttu-id="9b750-110">[out]返されるアイコンへのポインター。</span><span class="sxs-lookup"><span data-stu-id="9b750-110">[out] A pointer to the returned icon.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9b750-111">�߂�l</span><span class="sxs-lookup"><span data-stu-id="9b750-111">Return value</span></span>

<span data-ttu-id="9b750-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="9b750-112">S_OK</span></span> 
  
> <span data-ttu-id="9b750-113">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="9b750-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9b750-114">����</span><span class="sxs-lookup"><span data-stu-id="9b750-114">Remarks</span></span>

<span data-ttu-id="9b750-115">クライアント アプリケーションは、フォームのアイコンのプロパティのいずれかからアイコンを作成する**IMAPIFormInfo::MakeIconFromBinary**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9b750-115">Client applications call the **IMAPIFormInfo::MakeIconFromBinary** method to build an icon from one of the icon properties of a form.</span></span> <span data-ttu-id="9b750-116">_NPropID_パラメーターには、 **MakeIconFromBinary**は、フォームのアイコンのプロパティのいずれかのプロパティの識別子をかかります。</span><span class="sxs-lookup"><span data-stu-id="9b750-116">In the  _nPropID_ parameter, **MakeIconFromBinary** takes the property identifier of one of the icon properties of a form.</span></span> <span data-ttu-id="9b750-117">このプロパティの識別子を使用すると、アイコンのプロパティの列を含む表形式ビューで表示できるアイコンを構築します。</span><span class="sxs-lookup"><span data-stu-id="9b750-117">Using this property identifier, it builds an icon that can be displayed in table views that include property columns for icons.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9b750-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="9b750-118">See also</span></span>



[<span data-ttu-id="9b750-119">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="9b750-119">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)

