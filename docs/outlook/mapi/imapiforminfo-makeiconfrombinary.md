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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 418056f7222d5ab05f43a3661c1811bf2ae15be8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405115"
---
# <a name="imapiforminfomakeiconfrombinary"></a><span data-ttu-id="a6349-103">IMAPIFormInfo::MakeIconFromBinary</span><span class="sxs-lookup"><span data-stu-id="a6349-103">IMAPIFormInfo::MakeIconFromBinary</span></span>

  
  
<span data-ttu-id="a6349-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6349-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a6349-105">フォームのいずれかのアイコン プロパティからアイコンを作成します。</span><span class="sxs-lookup"><span data-stu-id="a6349-105">Builds an icon from one of the icon properties of a form.</span></span>
  
```cpp
HRESULT MakeIconFromBinary(
  ULONG nPropID,
  HICON FAR * phicon
);
```

## <a name="parameters"></a><span data-ttu-id="a6349-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a6349-106">Parameters</span></span>

 <span data-ttu-id="a6349-107">_nPropID_</span><span class="sxs-lookup"><span data-stu-id="a6349-107">_nPropID_</span></span>
  
> <span data-ttu-id="a6349-108">[in]icon プロパティのプロパティ識別子。</span><span class="sxs-lookup"><span data-stu-id="a6349-108">[in] A property identifier for an icon property.</span></span>
    
 <span data-ttu-id="a6349-109">_phicon_</span><span class="sxs-lookup"><span data-stu-id="a6349-109">_phicon_</span></span>
  
> <span data-ttu-id="a6349-110">[out]返されるアイコンへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a6349-110">[out] A pointer to the returned icon.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a6349-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="a6349-111">Return value</span></span>

<span data-ttu-id="a6349-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="a6349-112">S_OK</span></span> 
  
> <span data-ttu-id="a6349-113">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="a6349-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a6349-114">注釈</span><span class="sxs-lookup"><span data-stu-id="a6349-114">Remarks</span></span>

<span data-ttu-id="a6349-115">クライアント アプリケーションは **IMAPIFormInfo::MakeIconFromBinary** メソッドを呼び出して、フォームのアイコン プロパティの 1 つからアイコンを作成します。</span><span class="sxs-lookup"><span data-stu-id="a6349-115">Client applications call the **IMAPIFormInfo::MakeIconFromBinary** method to build an icon from one of the icon properties of a form.</span></span> <span data-ttu-id="a6349-116">_nPropID パラメーターで_**、MakeIconFromBinary は** フォームのアイコン プロパティの 1 つのプロパティ識別子を取得します。</span><span class="sxs-lookup"><span data-stu-id="a6349-116">In the  _nPropID_ parameter, **MakeIconFromBinary** takes the property identifier of one of the icon properties of a form.</span></span> <span data-ttu-id="a6349-117">このプロパティ識別子を使用すると、アイコンのプロパティ列を含むテーブル ビューに表示できるアイコンが作成されます。</span><span class="sxs-lookup"><span data-stu-id="a6349-117">Using this property identifier, it builds an icon that can be displayed in table views that include property columns for icons.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a6349-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="a6349-118">See also</span></span>



[<span data-ttu-id="a6349-119">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a6349-119">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)

