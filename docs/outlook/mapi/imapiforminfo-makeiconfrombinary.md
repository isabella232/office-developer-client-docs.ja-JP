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
ms.openlocfilehash: a230e8b69a64646dffb23147345d5960fdd38581
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800542"
---
# <a name="imapiforminfomakeiconfrombinary"></a><span data-ttu-id="ef94d-103">IMAPIFormInfo::MakeIconFromBinary</span><span class="sxs-lookup"><span data-stu-id="ef94d-103">IMAPIFormInfo::MakeIconFromBinary</span></span>

  
  
<span data-ttu-id="ef94d-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ef94d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ef94d-105">フォームのアイコンのプロパティのいずれかからアイコンを作成します。</span><span class="sxs-lookup"><span data-stu-id="ef94d-105">Builds an icon from one of the icon properties of a form.</span></span>
  
```cpp
HRESULT MakeIconFromBinary(
  ULONG nPropID,
  HICON FAR * phicon
);
```

## <a name="parameters"></a><span data-ttu-id="ef94d-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ef94d-106">Parameters</span></span>

 <span data-ttu-id="ef94d-107">_nPropID_</span><span class="sxs-lookup"><span data-stu-id="ef94d-107">_nPropID_</span></span>
  
> <span data-ttu-id="ef94d-108">[in]アイコンのプロパティにプロパティの識別子です。</span><span class="sxs-lookup"><span data-stu-id="ef94d-108">[in] A property identifier for an icon property.</span></span>
    
 <span data-ttu-id="ef94d-109">_phicon_</span><span class="sxs-lookup"><span data-stu-id="ef94d-109">_phicon_</span></span>
  
> <span data-ttu-id="ef94d-110">[out]返されるアイコンへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ef94d-110">[out] A pointer to the returned icon.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ef94d-111">�߂�l</span><span class="sxs-lookup"><span data-stu-id="ef94d-111">Return value</span></span>

<span data-ttu-id="ef94d-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="ef94d-112">S_OK</span></span> 
  
> <span data-ttu-id="ef94d-113">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="ef94d-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ef94d-114">����</span><span class="sxs-lookup"><span data-stu-id="ef94d-114">Remarks</span></span>

<span data-ttu-id="ef94d-115">クライアント アプリケーションは、フォームのアイコンのプロパティのいずれかからアイコンを作成する**IMAPIFormInfo::MakeIconFromBinary**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ef94d-115">Client applications call the **IMAPIFormInfo::MakeIconFromBinary** method to build an icon from one of the icon properties of a form.</span></span> <span data-ttu-id="ef94d-116">_NPropID_パラメーターには、 **MakeIconFromBinary**は、フォームのアイコンのプロパティのいずれかのプロパティの識別子をかかります。</span><span class="sxs-lookup"><span data-stu-id="ef94d-116">In the  _nPropID_ parameter, **MakeIconFromBinary** takes the property identifier of one of the icon properties of a form.</span></span> <span data-ttu-id="ef94d-117">このプロパティの識別子を使用すると、アイコンのプロパティの列を含む表形式ビューで表示できるアイコンを構築します。</span><span class="sxs-lookup"><span data-stu-id="ef94d-117">Using this property identifier, it builds an icon that can be displayed in table views that include property columns for icons.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ef94d-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="ef94d-118">See also</span></span>



[<span data-ttu-id="ef94d-119">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ef94d-119">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)

